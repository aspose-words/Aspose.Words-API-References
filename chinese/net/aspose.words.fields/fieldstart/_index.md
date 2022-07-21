---
title: FieldStart
second_title: Aspose.Words for .NET API 参考
description: 表示文档中 Word 字段的开始
type: docs
weight: 2280
url: /zh/net/aspose.words.fields/fieldstart/
---
## FieldStart class

表示文档中 Word 字段的开始。

```csharp
public class FieldStart : FieldChar
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata) { get; } | 获取与字段关联的自定义字段数据。 |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype) { get; } | 返回字段的类型。 |
| [Font](../../aspose.words/inline/font) { get; } | 提供对此对象的字体格式的访问。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | 如果此节点可以包含其他节点，则返回 true。 |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改 而不再正确（陈旧）。 |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | 如果启用更改跟踪时在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked) { get; set; } | 获取或设置父字段是否被锁定（不应重新计算其结果）。 |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | 返回 **真的**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。 |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | 返回 **真的**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟此节点的节点。 |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype) { get; } | 返回FieldStart. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | 检索父级[`Paragraph`](../../aspose.words/paragraph)这个节点的. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range) { get; } | 返回一个 **范围**表示此节点中包含的文档部分的对象。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept)(DocumentVisitor) | 接受访客。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | 获取指定对象类型的第一个祖先。 |
| [GetField](../../aspose.words.fields/fieldchar/getfield)() | 为字段 char 返回一个字段。 |
| override [GetText](../../aspose.words/specialchar/gettext)() | 获取此节点代表的特殊字符。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove)() | 从父级中移除自身。 |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

[`FieldStart`](../fieldstart)是一个内联级节点，由 the 表示[`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar)文档中的控制字符。

[`FieldStart`](../fieldstart)只能是[`Paragraph`](../../aspose.words/paragraph).

Microsoft Word 文档中的完整字段是一个复杂的结构，由 字段起始字符、字段代码、字段分隔符、字段结果 和字段结束字符组成。有些字段只有字段开始、字段代码和字段结束。

要轻松地将新字段插入到文档中，请使用[`InsertField`](../../aspose.words/documentbuilder/insertfield) 方法。

### 例子

展示如何使用字段集合。

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // 遍历字段集合，并打印内容和类型
    // 使用自定义访问者实现的每个字段。
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());

/// <summary>
/// 打印字段信息的文档访问者实现。
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// 获取访问者积累的文档的纯文本。
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// 在文档中遇到 FieldStart 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 FieldSeparator 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 FieldEnd 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

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

* class [FieldChar](../fieldchar)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
