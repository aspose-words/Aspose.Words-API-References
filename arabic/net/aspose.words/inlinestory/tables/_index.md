---
title: InlineStory.Tables
second_title: Aspose.Words لمراجع .NET API
description: InlineStory ملكية. الحصول على مجموعة من الجداول التي تعتبر أبناء القصة مباشرة.
type: docs
weight: 110
url: /ar/net/aspose.words/inlinestory/tables/
---
## InlineStory.Tables property

الحصول على مجموعة من الجداول التي تعتبر أبناء القصة مباشرة.

```csharp
public TableCollection Tables { get; }
```

### أمثلة

يوضح كيفية إدراج عقد InlineStory.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// تحتوي عقد الجدول على طريقة "EnsureMinimum()" التي تتأكد من أن الجدول يحتوي على خلية واحدة على الأقل.
Table table = new Table(doc);
table.EnsureMinimum();

// يمكننا وضع جدول داخل الحاشية السفلية، مما يجعله يظهر في تذييل الصفحة المرجعية.
Assert.That(footnote.Tables, Is.Empty);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// تحتوي InlineStory على طريقة "EnsureMinimum()" أيضًا، ولكن في هذه الحالة،
// يتأكد من أن الطفل الأخير للعقدة هو فقرة،
// لكي نتمكن من النقر على النص وكتابته بسهولة في Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// قم بتحرير مظهر المرساة، وهو رقم مرتفع صغير
// في النص الرئيسي الذي يشير إلى الحاشية السفلية.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// جميع عقد القصة المضمنة لها أنواع القصة الخاصة بها.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// التعليق هو نوع آخر من القصة المضمّنة.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// ستكون الفقرة الأصلية لعقدة القصة المضمنة هي الفقرة الموجودة في نص المستند الرئيسي.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// ومع ذلك، فإن الفقرة الأخيرة هي تلك الموجودة في محتوى نص التعليق،
// والذي سيكون خارج نص المستند الرئيسي في فقاعة الكلام.
// لن يحتوي التعليق على أي عقد فرعية بشكل افتراضي،
// حتى نتمكن من تطبيق طريقة EnsureMinimum() لوضع فقرة هنا أيضًا.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// بمجرد أن يكون لدينا فقرة، يمكننا تحريك المنشئ للقيام بذلك وكتابة تعليقنا.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### أنظر أيضا

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [InlineStory](../)
* مساحة الاسم [Aspose.Words](../../inlinestory/)
* المجسم [Aspose.Words](../../../)


