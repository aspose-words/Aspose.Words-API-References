---
title: CompareOptions.IgnoreTables
linktitle: IgnoreTables
articleTitle: IgnoreTables
second_title: Aspose.Words لـ .NET
description: CompareOptions IgnoreTables ملكية. يحدد ما إذا كان سيتم مقارنة الاختلافات في البيانات الموجودة في الجداول. بشكل افتراضي لا يتم تجاهل الجداول في C#.
type: docs
weight: 110
url: /ar/net/aspose.words.comparing/compareoptions/ignoretables/
---
## CompareOptions.IgnoreTables property

يحدد ما إذا كان سيتم مقارنة الاختلافات في البيانات الموجودة في الجداول. بشكل افتراضي لا يتم تجاهل الجداول.

```csharp
public bool IgnoreTables { get; set; }
```

## أمثلة

يوضح كيفية تصفية أنواع معينة من عناصر المستند عند إجراء المقارنة.

```csharp
// أنشئ المستند الأصلي واملأه بأنواع مختلفة من العناصر.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// نص الفقرة المشار إليه بتعليق ختامي:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// طاولة:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// مربع الكتابة:
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

// الرأس:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// أنشئ نسخة من المستند الخاص بنا وقم بإجراء تحرير سريع على كل عنصر من عناصر المستند المستنسخ.
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

// تؤدي مقارنة المستندات إلى إنشاء مراجعة لكل تعديل في المستند الذي تم تحريره.
// يحتوي كائن CompareOptions على سلسلة من العلامات التي يمكنها منع المراجعات
// على كل نوع من العناصر، مع تجاهل التغيير بشكل فعال.
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

### أنظر أيضا

* class [CompareOptions](../)
* مساحة الاسم [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* المجسم [Aspose.Words](../../../)
