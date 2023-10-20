---
title: Document.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words لـ .NET
description: Document Compare طريقة. يقارن هذا المستند بمستند آخر ينتج عنه تغييرات حسب عدد مراجعات التحرير والتنسيقRevision  في C#.
type: docs
weight: 560
url: /ar/net/aspose.words/document/compare/
---
## Compare(*[Document](../), string, DateTime*) {#compare}

يقارن هذا المستند بمستند آخر ينتج عنه تغييرات حسب عدد مراجعات التحرير والتنسيق[`Revision`](../../revision/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | وثيقة للمقارنة. |
| author | String | الأحرف الأولى من اسم المؤلف لاستخدامها في المراجعات. |
| dateTime | DateTime | التاريخ والوقت المستخدم للمراجعات. |

## ملاحظات

يجب ألا تحتوي المستندات على مراجعات قبل المقارنة.

## أمثلة

يوضح كيفية مقارنة المستندات.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// ستؤدي مقارنة المستندات مع المراجعات إلى حدوث استثناء.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// بعد المقارنة، سيحصل المستند الأصلي على مراجعة جديدة
// لكل عنصر مختلف في المستند المحرر.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// سيؤدي قبول هذه المراجعات إلى تحويل المستند الأصلي إلى المستند المحرر.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Compare(*[Document](../), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

يقارن هذا المستند بمستند آخر ينتج عنه تغييرات بعدد من مراجعات التحرير والتنسيق[`Revision`](../../revision/) . يسمح بتحديد خيارات المقارنة باستخدام[`CompareOptions`](../../../aspose.words.comparing/compareoptions/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
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

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
