---
title: CompareOptions.IgnoreTextboxes
linktitle: IgnoreTextboxes
articleTitle: IgnoreTextboxes
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية CompareOptions IgnoreTextboxes على تعزيز مقارنة البيانات من خلال استبعاد الاختلافات في مربع النص للحصول على نتائج أكثر دقة.
type: docs
weight: 120
url: /ar/net/aspose.words.comparing/compareoptions/ignoretextboxes/
---
## CompareOptions.IgnoreTextboxes property

يحدد ما إذا كان سيتم مقارنة الاختلافات في البيانات الموجودة داخل مربعات النص.

```csharp
public bool IgnoreTextboxes { get; set; }
```

## ملاحظات

افتراضيًا، لا يتم تجاهل مربعات النص.

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

* class [CompareOptions](../)
* مساحة الاسم [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* المجسم [Aspose.Words](../../../)
