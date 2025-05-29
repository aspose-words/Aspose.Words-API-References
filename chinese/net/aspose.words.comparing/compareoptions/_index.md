---
title: CompareOptions Class
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.CompareOptions 类，实现高级文档比较。自定义比较设置，获得精确结果并提高工作效率。
type: docs
weight: 470
url: /zh/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

允许选择文档比较操作的附加选项。

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
| [AdvancedOptions](../../aspose.words.comparing/compareoptions/advancedoptions/) { get; } | 指定高级比较选项，可能有助于产生更精确的比较输出。 |
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | 指定是否比较两个文档之间的差异。 |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | 指定是否按字符或按字跟踪更改。 |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True 表示文档比较不区分大小写。 |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | 指定是否比较注释中的差异。 |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | 指定是否比较字段中的差异。 |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | 指定是否比较脚注和尾注的差异。 |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | True 表示忽略格式。 |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | True 表示忽略页眉和页脚内容。 |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | 指定是否比较表中包含的数据的差异。 |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | 指定是否比较文本框内包含的数据的差异。 |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | 指定在比较期间应使用哪个文档作为目标。 |

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

* 命名空间 [Aspose.Words.Comparing](../../aspose.words.comparing/)
* 部件 [Aspose.Words](../../)
