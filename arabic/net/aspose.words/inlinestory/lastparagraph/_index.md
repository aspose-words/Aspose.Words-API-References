---
title: InlineStory.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية InlineStory LastParagraph للوصول بسهولة إلى الفقرة الأخيرة من قصتك، مما يعزز تجربة إدارة المحتوى لديك.
type: docs
weight: 70
url: /ar/net/aspose.words/inlinestory/lastparagraph/
---
## InlineStory.LastParagraph property

يحصل على الفقرة الأخيرة في القصة.

```csharp
public Paragraph LastParagraph { get; }
```

## أمثلة

يوضح كيفية إدراج عقد InlineStory.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// تحتوي عقد الجدول على طريقة "EnsureMinimum()" التي تتأكد من أن الجدول يحتوي على خلية واحدة على الأقل.
Table table = new Table(doc);
table.EnsureMinimum();

//يمكننا وضع جدول داخل الحاشية السفلية، مما سيجعله يظهر في تذييل الصفحة المرجعية.
Assert.AreEqual(0, footnote.Tables.Count);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// تحتوي InlineStory أيضًا على طريقة "EnsureMinimum()"، ولكن في هذه الحالة،
// يتأكد من أن آخر طفل للعقدة هو فقرة،
// حتى نتمكن من النقر وكتابة النص بسهولة في Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// تعديل مظهر المرساة، وهو الرقم العلوي الصغير
// في النص الرئيسي الذي يشير إلى الحاشية السفلية.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// جميع عقد القصة المضمنة لها أنواع القصة الخاصة بها.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

//التعليق هو نوع آخر من القصة المضمنة.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// ستكون الفقرة الأصلية لعقدة القصة المضمنة هي الفقرة الموجودة في نص المستند الرئيسي.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// ومع ذلك، فإن الفقرة الأخيرة هي الفقرة الموجودة في محتوى نص التعليق،
// والتي ستكون خارج نص المستند الرئيسي في فقاعة الكلام.
// لن يحتوي التعليق على أي عقد فرعية بشكل افتراضي،
// حتى نتمكن من تطبيق طريقة EnsureMinimum() لوضع فقرة هنا أيضًا.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// بمجرد أن نحصل على فقرة، يمكننا تحريك المنشئ للقيام بذلك وكتابة تعليقنا.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### أنظر أيضا

* class [Paragraph](../../paragraph/)
* class [InlineStory](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
