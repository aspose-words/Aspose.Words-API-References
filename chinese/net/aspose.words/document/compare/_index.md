---
title: Document.Compare
linktitle: Compare
articleTitle: Compare
second_title: 用于 .NET 的 Aspose.Words
description: Document Compare 方法. 将此文档与另一个文档进行比较以产生编辑和格式修订的数量Revision 在 C#.
type: docs
weight: 560
url: /zh/net/aspose.words/document/compare/
---
## Compare(*[Document](../), string, DateTime*) {#compare}

将此文档与另一个文档进行比较，以产生编辑和格式修订的数量[`Revision`](../../revision/).

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | Document | 要比较的文档。 |
| author | String | 用于修订的作者姓名缩写。 |
| dateTime | DateTime | 用于修订的日期和时间。 |

## 评论

暂时不比较以下文档节点：

* [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)
* 第 3 项

文件在比较前不得有修改。

## 例子

显示如何比较文档。

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// 比较文档和修订版本会抛出异常。
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// 比较后，原文档会得到一个新的修订版
// 对于已编辑文档中不同的每个元素。
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// 接受这些修订会将原始文档转换为编辑后的文档。
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Compare(*[Document](../), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

将此文档与另一个文档进行比较，从而产生大量编辑和格式修订[`Revision`](../../revision/). 允许使用指定比较选项[`CompareOptions`](../../../aspose.words.comparing/compareoptions/).

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

## 例子

显示如何在进行比较时过滤特定类型的文档元素。

```csharp
// 创建原始文档并用各种元素填充它。
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// 使用尾注引用的段落文本：
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

// 创建我们文档的克隆并对每个克隆文档的元素执行快速编辑。
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

// 比较文档会为已编辑文档中的每个编辑创建一个修订。
// CompareOptions 对象有一系列可以抑制修订的标志
// 在每种类型的元素上，有效地忽略它们的变化。
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreFormatting = false;
compareOptions.IgnoreCaseChanges = false;
compareOptions.IgnoreComments = false;
compareOptions.IgnoreTables = false;
compareOptions.IgnoreFields = false;
compareOptions.IgnoreFootnotes = false;
compareOptions.IgnoreTextboxes = false;
compareOptions.IgnoreHeadersAndFooters = false;
compareOptions.Target = ComparisonTargetType.New;

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Document.CompareOptions.docx");
```

### 也可以看看

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
