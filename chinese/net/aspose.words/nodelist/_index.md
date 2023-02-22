---
title: Class NodeList
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.NodeList 班级. 表示与使用执行的 XPath 查询匹配的节点集合SelectNodes方法.
type: docs
weight: 3980
url: /zh/net/aspose.words/nodelist/
---
## NodeList class

表示与使用执行的 XPath 查询匹配的节点集合[`SelectNodes`](../compositenode/selectnodes/)方法.

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
| [ToArray](../../aspose.words/nodelist/toarray/)() | 将集合中的所有节点复制到新的节点数组中。 |

### 评论

**节点列表**由返回[`SelectNodes`](../compositenode/selectnodes/)并包含与 XPath 查询匹配的节点的 collection 。

**节点列表**支持索引访问和迭代。

对待 **节点列表**集合作为“快照”集合。 **节点列表**开始 作为“实时”集合，因为在运行 XPath 查询时实际上并未检索节点。 仅在访问时检索节点，此时节点和在它之前的所有节点 被缓存形成“快照”集合。

### 例子

演示如何在 Word 文档中查找所有超链接，然后更改其 URL 和显示名称。

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
            NodeList fieldStarts = doc.SelectNodes("//FieldStart");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // 链接到书签的超链接没有 URL。
                    if (hyperlink.IsLocal)
                        continue;

                    // 给每个 URL 超链接一个新的 URL 和名称。
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

    /// <summary>
    /// HYPERLINK 字段包含并显示文档正文中的超链接。 Aspose.Words 中的一个字段 
    /// 由几个节点组成，可能很难直接使用所有这些节点。 
    /// 仅当超链接代码和名称均仅包含一个运行节点时，此实现才有效。
    ///
    /// 字段的节点结构如下：
    /// 
    /// [FieldStart][Run - 域代码][FieldSeparator][Run - 域结果][FieldEnd]
    /// 
    /// 下面是 HYPERLINK 字段的两个示例字段代码：
    /// 超链接“网址”
    /// HYPERLINK \l "书签名称"
    /// 
    /// 字段的“结果”属性包含该字段在文档正文中向用户显示的文本。
    /// </summary>
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

            // 正常情况下，我们总能找到字段的结束节点，但是示例文档 
            // 在超链接中包含一个分段符，将字段置于末尾 
            // 在下一段中。处理跨越多个领域的字段会复杂得多 
            // 段落正确。在这种情况下，允许字段 end 为空就足够了。
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // 域代码类似于“HYPERLINK”http:\\www.myurl.com“”，但它可以包含多个运行。
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // 如果域代码中存在 \l，则超链接是本地的。
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

        /// <summary>
        /// 获取或设置超链接的显示名称。
        /// </summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                // 超链接显示名称存储在字段结果中，即一个Run 
                // 字段分隔符和字段结束之间的节点。
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // 如果字段结果包含多个运行，则删除这些运行。
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

        /// <summary>
        /// 获取或设置超链接的目标 URL 或书签名称。
        /// </summary>
        internal string Target
        {
            get => mTarget;
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

        /// <summary>
        /// 如果超链接目标是文档内的书签，则为真。如果超链接是 URL，则为 False。
        /// </summary>
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
            // 字段的字段代码位于字段起始节点和字段分隔符之间的运行节点中。
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // 如果域代码包含多个运行，则删除这些运行。
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

        /// <summary>
        /// 从起始节点开始遍历兄弟节点，直到找到指定类型或 null 的节点。
        /// </summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

        /// <summary>
        /// 检索从开始到但不包括结束节点的文本。
        /// </summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

        /// <summary>
        /// 删除从开始到但不包括结束节点的节点。
        /// 假设起始节点和结束节点具有相同的父节点。
        /// </summary>
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
            "\\S+" + // 一个或多个非空格 HYPERLINK 或其他语言的其他单词。
            "\\s+" + // 一个或多个空格。
            "(?:\"\"\\s+)?" + // 非捕获可选的 "" 和一个或多个空格。
            "(\\\\l\\s+)?" + // 可选的 \l 标志，后跟一个或多个空格。
            "\"" + // 一个撇号。    
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


