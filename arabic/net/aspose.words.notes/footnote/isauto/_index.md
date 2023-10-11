---
title: Footnote.IsAuto
second_title: Aspose.Words لمراجع .NET API
description: Footnote ملكية. يحمل قيمة تحدد ما إذا كانت هذه حاشية سفلية مرقمة تلقائيًا أو حاشية سفلية بعلامة مرجعية مخصصة يحددها المستخدم.
type: docs
weight: 30
url: /ar/net/aspose.words.notes/footnote/isauto/
---
## Footnote.IsAuto property

يحمل قيمة تحدد ما إذا كانت هذه حاشية سفلية مرقمة تلقائيًا أو حاشية سفلية بعلامة مرجعية مخصصة يحددها المستخدم.

```csharp
public bool IsAuto { get; set; }
```

### ملاحظات

[`ReferenceMark`](../referencemark/)تمت تهيئته بسلسلة فارغة إذا`IsAuto` ضبط ل`خطأ شنيع` .

### أمثلة

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

* class [Footnote](../)
* مساحة الاسم [Aspose.Words.Notes](../../footnote/)
* المجسم [Aspose.Words](../../../)


