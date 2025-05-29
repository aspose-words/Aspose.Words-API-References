---
title: ComparisonTargetType Enum
linktitle: ComparisonTargetType
articleTitle: ComparisonTargetType
second_title: Aspose.Words لـ .NET
description: اكتشف مُعدّل Aspose.Words ComparisonTargetType لمقارنات مستندات دقيقة. حدّد مستندك الأساسي بسهولة للحصول على نتائج دقيقة. ابدأ التحسين الآن!
type: docs
weight: 480
url: /ar/net/aspose.words.comparing/comparisontargettype/
---
## ComparisonTargetType enumeration

يسمح بتحديد المستند الأساسي الذي سيتم استخدامه أثناء المقارنة. القيمة الافتراضية هيCurrent .

```csharp
public enum ComparisonTargetType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Current | `0` | يتم استخدام هذه الوثيقة كأساس أثناء المقارنة. |
| New | `1` | يتم استخدام مستند آخر كأساس أثناء المقارنة. |

## ملاحظات

يتعلق بخيار "إظهار التغييرات في" في Microsoft Word في مربع الحوار "مقارنة المستندات".

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
