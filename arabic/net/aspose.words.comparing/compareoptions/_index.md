---
title: CompareOptions Class
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.CompareOptions لمقارنة المستندات المتقدمة. خصّص إعدادات المقارنة للحصول على نتائج دقيقة وإنتاجية مُحسّنة.
type: docs
weight: 470
url: /ar/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

يسمح باختيار خيارات إضافية لعملية مقارنة المستندات.

لمعرفة المزيد، قم بزيارة[مقارنة المستندات](https://docs.aspose.com/words/net/compare-documents/) مقالة توثيقية.

```csharp
public class CompareOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CompareOptions](compareoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AdvancedOptions](../../aspose.words.comparing/compareoptions/advancedoptions/) { get; } | يحدد خيارات المقارنة المتقدمة التي قد تساعد في إنتاج مخرجات مقارنة أكثر دقة. |
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | يحدد ما إذا كان سيتم مقارنة الاختلافات بين المستندين. |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | يحدد ما إذا كان سيتم تعقب التغييرات حسب الحرف أو حسب الكلمة. |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | يشير True إلى أن مقارنة المستندات لا تميز بين الأحرف الكبيرة والصغيرة. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | يحدد ما إذا كان سيتم مقارنة الاختلافات في التعليقات. |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | يحدد ما إذا كان سيتم مقارنة الاختلافات في الحقول. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | يحدد ما إذا كان سيتم مقارنة الاختلافات في الحواشي السفلية والختامية. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | يشير True إلى أن التنسيق يتم تجاهله. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | يشير True إلى تجاهل محتوى الرؤوس والتذييلات. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | يحدد ما إذا كان سيتم مقارنة الاختلافات في البيانات الموجودة في الجداول. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | يحدد ما إذا كان سيتم مقارنة الاختلافات في البيانات الموجودة داخل مربعات النص. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | يحدد المستند الذي سيتم استخدامه كهدف أثناء المقارنة. |

## أمثلة

يوضح كيفية تصفية أنواع معينة من عناصر المستند عند إجراء مقارنة.

```csharp
// قم بإنشاء المستند الأصلي واملأه بأنواع مختلفة من العناصر.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// نص الفقرة المشار إليها مع حاشية ختامية:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// طاولة:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// مربع النص:
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// حقل التاريخ:
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// تعليق:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

//العنوان:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// قم بإنشاء نسخة من مستندنا وقم بإجراء تحرير سريع على كل عنصر من عناصر المستند المستنسخ.
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

// تؤدي مقارنة المستندات إلى إنشاء مراجعة لكل تعديل في المستند المحرر.
// يحتوي كائن CompareOptions على سلسلة من العلامات التي يمكنها قمع المراجعات
// على كل نوع من العناصر، وتجاهل التغيير الذي يحدث لهم بشكل فعال.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Comparing](../../aspose.words.comparing/)
* المجسم [Aspose.Words](../../)
