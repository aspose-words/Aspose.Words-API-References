---
title: CompareOptions Class
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Comparing.CompareOptions 班级. 允许选择文档比较操作的高级选项 在 C#.
type: docs
weight: 270
url: /zh/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

允许选择文档比较操作的高级选项。

要了解更多信息，请访问[比较文档](https://docs.aspose.com/words/net/compare-documents/)文档文章。

```csharp
public class CompareOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CompareOptions](compareoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | 指定是否比较差异MoveRevision两个文档之间。 默认情况下不会生成移动修订版。 |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | 指定是按字符还是按单词跟踪更改。 默认值为WordLevel. |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True 表示文档比较不区分大小写。 默认情况下比较区分大小写。 |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | 指定是否比较注释中的差异。 默认情况下不忽略注释。 |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid/) { get; set; } | 指定是否忽略 DrawingML 唯一 ID 中的差异。 默认值为`错误的`. |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | 指定是否比较字段中的差异。 默认情况下不忽略字段。 |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | 指定是否比较脚注和尾注的差异。 默认情况下不忽略脚注。 |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | True 表示忽略格式设置。 默认情况下，不忽略文档格式设置。 |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | True 表示忽略页眉和页脚内容。 默认情况下不忽略页眉和页脚。 |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | 指定是否比较表中包含的数据差异。 默认情况下不忽略表。 |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | 指定是否比较文本框中包含的数据的差异。 默认情况下，不忽略文本框。 |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | 指定比较期间应使用哪个文档作为目标。 |

## 例子

演示如何在进行比较时过滤特定类型的文档元素。

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

// 标头：
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// 创建文档的克隆并对克隆文档的每个元素执行快速编辑。
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

// 比较文档会为已编辑文档中的每个编辑创建修订。
// CompareOptions 对象具有一系列可以抑制修订的标志
// 在每种类型的元素上，有效地忽略它们的更改。
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

* 命名空间 [Aspose.Words.Comparing](../../aspose.words.comparing/)
* 部件 [Aspose.Words](../../)
