---
title: NodeList Class
linktitle: NodeList
articleTitle: NodeList
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.NodeList 班级. 表示与使用以下命令执行的 XPath 查询匹配的节点集合SelectNodes方法 在 C#.
type: docs
weight: 4220
url: /zh/net/aspose.words/nodelist/
---
## NodeList class

表示与使用以下命令执行的 XPath 查询匹配的节点集合[`SelectNodes`](../compositenode/selectnodes/)方法.

要了解更多信息，请访问[Aspose.Words 文档对象模型 (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

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
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | 在节点集合上提供简单的“foreach”样式迭代。 |
| [ToArray](../../aspose.words/nodelist/toarray/)() | 将集合中的所有节点复制到新的节点数组。 |

## 评论

`NodeList`由返回[`SelectNodes`](../compositenode/selectnodes/)并包含与 XPath 查询匹配的节点的集合 。

`NodeList`支持索引访问和迭代。

治疗`NodeList`集合作为“快照”集合。`NodeList`将 启动为“实时”集合，因为运行XPath 查询时实际上并未检索节点。 仅在访问时检索节点，此时该节点和 之前的所有节点都被缓存，形成“快照”集合。

## 例子

演示如何查找 Word 文档中的所有超链接，然后更改其 URL 和显示名称。

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

                    // 为每个 URL 超链接指定一个新的 URL 和名称。
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

     ///<summary>
      ///HYPERLINK 字段包含并显示文档正文中的超链接。 Aspose.Words 中的字段
     ///由多个节点组成，直接使用所有这些节点可能很困难。
     ///仅当超链接代码和名称仅包含一个运行节点时，此实现才有效。
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

            // 找到字段分隔符节点。
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // 通常情况下，我们总能找到字段的结束节点，但是示例文档
            // 在超链接内包含段落分隔符，这会将字段置于末尾
            // 在下一段中。处理跨多个字段的情况会复杂得多
            // 段落正确。在这种情况下，允许字段结束为空就足够了。
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // 字段代码看起来类似于“HYPERLINK "http:\\www.myurl.com"”，但它可以由多次运行组成。
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
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                 // 超链接显示名称存储在字段result中，该字段是一个Run
                // 字段分隔符和字段结束之间的节点。
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // 如果字段结果包含多个运行，则删除这些运行。
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

         ///<summary>
         ///Gets or sets the target URL or bookmark name of the hyperlink.
         ///</summary>
        internal string Target
        {
            get => mTarget;
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
            get => mIsLocal; 
            set
            {
                mIsLocal = value;
                UpdateFieldCode();
            }
        }

        private void UpdateFieldCode()
        {
            // 字段的字段代码位于字段起始节点和字段分隔符之间的 Run 节点中。
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // 如果字段代码包含多个运行，则删除这些运行。
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
            "\\S+" + // 一个或多个非空格超链接或其他语言中的其他单词。
            "\\s+" + // 一个或多个空格。
            "(?:\"\"\\s+)?" + // 不捕获可选的“”和一个或多个空格。
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
