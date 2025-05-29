---
title: NodeList Class
linktitle: NodeList
articleTitle: NodeList
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.NodeList 类，这是高效管理 XPath 查询结果和增强文档处理能力的首选解决方案。
type: docs
weight: 4910
url: /zh/net/aspose.words/nodelist/
---
## NodeList class

表示与使用以下方法执行的 XPath 查询匹配的节点集合[`SelectNodes`](../compositenode/selectnodes/)方法.

要了解更多信息，请访问[Aspose.Words 文档对象模型（DOM）](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class NodeList : IEnumerable<Node>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | 获取列表中的节点数。 |
| [Item](../../aspose.words/nodelist/item/) { get; } | 检索给定索引处的节点。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | 提供对节点集合的简单“foreach”样式迭代。 |
| [ToArray](../../aspose.words/nodelist/toarray/)() | 将集合中的所有节点复制到新的节点数组。 |

## 评论

`NodeList`返回的是[`SelectNodes`](../compositenode/selectnodes/)并包含与 XPath 查询匹配的节点 collection 。

`NodeList`支持索引访问和迭代。

治疗`NodeList`集合作为“快照”集合。`NodeList` starts 作为“实时”集合，因为运行 XPath 查询时实际上并未检索节点。 仅在访问时检索节点，此时该节点和其之前的所有节点都被缓存，形成“快照”集合。

## 例子

展示如何查找 Word 文档中的所有超链接，然后更改它们的 URL 和显示名称。

```csharp
using System;
using System.Linq;
using System.Text;
using System.Text.RegularExpressions;
using Aspose.Words;
using Aspose.Words.Fields;
using NUnit.Framework;

namespace ApiExamples
{
    public class ExReplaceHyperlinks : ApiExampleBase
    {
        public void Fields()
        {
            Document doc = new Document(MyDir + "Hyperlinks.docx");

            // Word 文档中的超链接是字段。要开始查找超链接，我们必须首先找到所有字段。
            // 使用“SelectNodes”方法通过 XPath 查找文档中的所有字段。
            NodeList fieldStarts = doc.SelectNodes("//字段开始");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // 链接到书签的超链接没有 URL。
                    if (hyperlink.IsLocal)
                        continue;

                    // 为每个 URL 超链接赋予一个新的 URL 和名称。
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com”;
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

     ///<summary>
      ///HYPERLINK 字段包含并显示文档正文中的超链接。Aspose.Words 中的一个字段
     ///由多个节点组成，直接处理所有这些节点可能会很困难。
     ///仅当超链接代码和名称各自仅由一个 Run 节点组成时，此实现才会有效。
    ///
     ///字段的节点结构如下：
     ///
     ///[FieldStart][Run - field code][FieldSeparator][Run - field result][FieldEnd]
     ///
     ///Below are two example field codes of HYPERLINK fields:
     ///HYPERLINK "url"
     ///HYPERLINK \l "bookmark name"
     ///
     ///A field's "Result" property contains text that the field displays in the document body to the user.
     ///</summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // 查找字段分隔符节点。
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // 正常情况下，我们总能找到字段的结束节点，但示例文档
            // 包含超链接内的段落分隔符，使字段结束
            // 在下一段中。处理跨越多个字段会更加复杂
            // 段落正确。在这种情况下，允许字段 end 为空就足够了。
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // 字段代码看起来像“HYPERLINK“http:\\www.myurl.com””，但它可以由多次运行组成。
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // 如果字段代码中存在 \l，则超链接是本地的。
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

         ///<summary>
         ///Gets or sets the display name of the hyperlink.
         ///</summary>
        internal string Name
        {
            get
            {
                return GetTextSameParent(mFieldSeparator, mFieldEnd);
            }
            set
            {
                 // 超链接显示名称存储在字段 result 中，该字段为 Run
                // 字段分隔符和字段结尾之间的节点。
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // 如果字段结果由多个运行组成，则删除这些运行。
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

         ///<summary>
         ///Gets or sets the target URL or bookmark name of the hyperlink.
         ///</summary>
        internal string Target
        {
            get
            {
                return mTarget;
            }
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

         ///<summary>
         ///True if the hyperlinks target is a bookmark inside the document. False if the hyperlink is a URL.
         ///</summary>
        internal bool IsLocal
        {
            get
            {
                return mIsLocal;
            }
            set
            {
                mIsLocal = value;
                UpdateFieldCode();
            }
        }

        private void UpdateFieldCode()
        {
            // 字段的字段代码位于字段的起始节点和字段分隔符之间的 Run 节点中。
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // 如果字段代码由多个运行组成，则删除这些运行。
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

         ///<summary>
         ///Goes through siblings starting from the start node until it finds a node of the specified type or null.
         ///</summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

         ///<summary>
         ///Retrieves text from start up to but not including the end node.
         ///</summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

         ///<summary>
         ///Removes nodes from start up to but not including the end node.
         ///Assumes that the start and end nodes have the same parent.
         ///</summary>
        private static void RemoveSameParent(Node startNode, Node endNode)
        {
            if (endNode != null && startNode.ParentNode != endNode.ParentNode)
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            Node curChild = startNode;
            while ((curChild != null) && (curChild != endNode))
            {
                Node nextChild = curChild.NextSibling;
                curChild.Remove();
                curChild = nextChild;
            }
        }

        private readonly Node mFieldStart;
        private readonly Node mFieldSeparator;
        private readonly Node mFieldEnd;
        private bool mIsLocal;
        private string mTarget;

        private static readonly Regex gRegex = new Regex(
            "\\S+" + // 一个或多个非空格 HYPERLINK 或其他语言中的其他单词。
            "\\s+" + // 一个或多个空格。
            "(?:\"\"\\s+)?" + // 非捕获可选的“”和一个或多个空格。
            "(\\\\l\\s+)?" + // 可选的 \l 标志后跟一个或多个空格。
            "\"" +  // 一个撇号。
            "([^\"]+)" + // 一个或多个字符，不包括撇号（超链接目标）。
            "\"" // 一个结束撇号。
        );
    }
}
```

### 也可以看看

* class [Node](../node/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
