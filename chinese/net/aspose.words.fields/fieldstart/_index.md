---
title: FieldStart Class
linktitle: FieldStart
articleTitle: FieldStart
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldStart 类，高效管理文档中 Word 字段的关键。立即增强您的文档处理能力！
type: docs
weight: 2840
url: /zh/net/aspose.words.fields/fieldstart/
---
## FieldStart class

表示文档中 Word 字段的开始。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldStart : FieldChar
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | 获取与该字段关联的自定义字段数据。 |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | 返回字段的类型。 |
| [Font](../../aspose.words/inline/font/) { get; } | 提供对此对象的字体格式的访问。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | 返回`真的`如果此节点可以包含其他节点。 |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（过时）。 |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | 如果在启用更改跟踪的情况下 Microsoft Word 中的对象格式发生更改，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入 Microsoft Word，则返回 true。 |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | 获取或设置父字段是否被锁定（不应重新计算其结果）。 |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | 返回FieldStart. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | 检索父级[`Paragraph`](../../aspose.words/paragraph/)此节点的。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | 返回字段 char. 的字段 |
| override [GetText](../../aspose.words/specialchar/gettext/)() | 获取此节点代表的特殊字符。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

## 评论

`FieldStart`是内联级别节点，由 表示[`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/)文档中的控制字符。

`FieldStart`只能是[`Paragraph`](../../aspose.words/paragraph/)。

Microsoft Word 文档中一个完整的字段是一个复杂的结构，由字段起始符、字段代码、字段分隔符、字段结果和字段结束符组成。有些字段只有字段起始符、字段代码和字段结束符。

要轻松地将新字段插入文档，请使用[`InsertField`](../../aspose.words/documentbuilder/insertfield/) 方法。

## 例子

展示如何处理字段集合。

```csharp
public void FieldCollection()
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
}

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
    /// 当在文档中遇到 FieldStart 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 FieldSeparator 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 FieldEnd 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

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

* class [FieldChar](../fieldchar/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
