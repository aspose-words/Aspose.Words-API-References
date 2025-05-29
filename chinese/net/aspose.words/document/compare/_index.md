---
title: Document.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words for .NET
description: 使用我们的文档比较工具轻松比较文档。快速识别编辑和格式更改，从而简化修订流程并增强协作。
type: docs
weight: 600
url: /zh/net/aspose.words/document/compare/
---
## Compare(*[Document](../), string, DateTime*) {#compare}

将此文档与另一个文档进行比较，得出编辑次数和格式修订的变化[`Revision`](../../revision/).

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | Document | 要比较的文档。 |
| author | String | 用于修订的作者姓名首字母。 |
| dateTime | DateTime | 用于修订的日期和时间。 |

## 评论

文档在比较之前不得有修改。

## 例子

显示如何比较文档。

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// 将文档与修订版本进行比较将会引发异常。
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// 比较后，原始文档将获得新的修订版本
// 对于编辑文档中每个不同的元素。
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// 接受这些修订将把原始文档转换为编辑后的文档。
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Compare(*[Document](../), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

将此文档与另一文档进行比较，产生许多编辑和格式修订[`Revision`](../../revision/). 允许使用指定比较选项[`CompareOptions`](../../../aspose.words.comparing/compareoptions/).

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

## 例子

展示如何在进行比较时过滤特定类型的文档元素。

```csharp
// 创建原始文档并用各种元素填充它。
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// 带有尾注引用的段落文本：
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// 桌子：
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// 文本框：
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// 日期字段：
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// 评论：
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// 标题：
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// 创建我们文档的克隆并对克隆文档的每个元素执行快速编辑。
Document docEdited = (Document)docOriginal.Clone(true);
Paragraph firstParagraph = docEdited.FirstSection.Body.FirstParagraph;

firstParagraph.Runs[0].Text = "hello world! this is the first paragraph, after editing.";
firstParagraph.ParagraphFormat.Style = docEdited.Styles[StyleIdentifier.Heading1];
((Footnote)docEdited.GetChild(NodeType.Footnote, 0, true)).FirstParagraph.Runs[1].Text = "Edited endnote text.";
((Table)docEdited.GetChild(NodeType.Table, 0, true)).FirstRow.Cells[1].FirstParagraph.Runs[0].Text = "Edited Cell 2 contents";
((Shape)docEdited.GetChild(NodeType.Shape, 0, true)).FirstParagraph.Runs[0].Text = "Edited textbox contents";
((FieldDate)docEdited.Range.Fields[0]).UseLunarCalendar = true;
((Comment)docEdited.GetChild(NodeType.Comment, 0, true)).FirstParagraph.Runs[0].Text = "Edited comment.";
docEdited.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].FirstParagraph.Runs[0].Text =
    "Edited header contents.";

// 比较文档会为编辑文档中的每个编辑创建修订。
// CompareOptions 对象有一系列可以抑制修订的标志
// 对每种类型的元素进行相应处理，有效地忽略它们的变化。
CompareOptions compareOptions = new CompareOptions
{
    CompareMoves = false,
    IgnoreFormatting = false,
    IgnoreCaseChanges = false,
    IgnoreComments = false,
    IgnoreTables = false,
    IgnoreFields = false,
    IgnoreFootnotes = false,
    IgnoreTextboxes = false,
    IgnoreHeadersAndFooters = false,
    Target = ComparisonTargetType.New
};

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Revision.CompareOptions.docx");
```

### 也可以看看

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
