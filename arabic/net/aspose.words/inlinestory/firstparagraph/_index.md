---
title: InlineStory.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words لـ .NET
description: InlineStory FirstParagraph ملكية. الحصول على الفقرة الأولى في القصة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/inlinestory/firstparagraph/
---
## InlineStory.FirstParagraph property

الحصول على الفقرة الأولى في القصة.

```csharp
public Paragraph FirstParagraph { get; }
```

## أمثلة

يوضح كيفية إضافة تعليق إلى فقرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // في Microsoft Word، يمكننا النقر بزر الماوس الأيمن فوق هذا التعليق في نص المستند لتحريره أو الرد عليه.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

يوضح كيفية إدراج الحواشي السفلية وتخصيصها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف نصًا، وأشر إليه بحاشية سفلية. ستضع هذه الحاشية السفلية مرجعًا مرتفعًا صغيرًا
// ضع علامة بعد النص الذي تشير إليه وقم بإنشاء إدخال أسفل النص الأساسي في أسفل الصفحة.
// سيحتوي هذا الإدخال على العلامة المرجعية للحاشية السفلية والنص المرجعي،
// والذي سنمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// إذا تم تعيين هذه الخاصية على "صحيح"، فستكون العلامة المرجعية للحاشية السفلية
// سيكون فهرسه بين جميع الحواشي السفلية للقسم.
// هذه هي الحاشية السفلية الأولى، لذا ستكون العلامة المرجعية "1".
Assert.True(footnote.IsAuto);

 // يمكننا نقل أداة إنشاء المستندات داخل الحاشية السفلية لتحرير النص المرجعي الخاص بها.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// يمكننا تعيين علامة مرجعية مخصصة تستخدمها الحاشية السفلية بدلاً من رقم الفهرس الخاص بها.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// الإشارة المرجعية التي تم ضبط علامة "IsAuto" على "صحيح" ستظل تُظهر فهرسها الحقيقي
// حتى لو كانت الإشارات المرجعية السابقة تعرض علامات مرجعية مخصصة، فستكون العلامة المرجعية لهذه الإشارة المرجعية "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### أنظر أيضا

* class [Paragraph](../../paragraph/)
* class [InlineStory](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
