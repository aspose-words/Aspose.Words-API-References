---
title: Footnote.IsAuto
linktitle: IsAuto
articleTitle: IsAuto
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsAuto للحواشي السفلية، والتي تتيح ترقيمًا تلقائيًا سلسًا أو علامات مرجعية مخصصة لتحسين وضوح المستند وتنظيمه.
type: docs
weight: 40
url: /ar/net/aspose.words.notes/footnote/isauto/
---
## Footnote.IsAuto property

تحتوي على قيمة تحدد ما إذا كانت هذه حاشية سفلية مرقمة تلقائيًا أو حاشية سفلية مع علامة مرجعية مخصصة يحددها المستخدم.

```csharp
public bool IsAuto { get; set; }
```

## ملاحظات

[`ReferenceMark`](../referencemark/) تم تهيئة الأمر بسلسلة فارغة إذا`IsAuto` تم ضبطه على`خطأ شنيع` .

## أمثلة

يوضح كيفية إدراج الحواشي السفلية وتخصيصها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف نصًا، وأشر إليه بحاشية سفلية. ستُضيف هذه الحاشية إشارة علوية صغيرة.
// ضع علامة بعد النص الذي تشير إليه وقم بإنشاء إدخال أسفل نص الهيئة الرئيسي في أسفل الصفحة.
// سيحتوي هذا الإدخال على علامة مرجع الحاشية السفلية ونص المرجع،
// والتي سنمررها إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// إذا تم تعيين هذه الخاصية على "true"، فسيتم استخدام علامة مرجع الحاشية السفلية لدينا
//سيكون فهرسها بين جميع حواشي القسم.
// هذه هي الحاشية الأولى، لذا فإن علامة المرجع ستكون "1".
Assert.True(footnote.IsAuto);

 // يمكننا نقل منشئ المستند داخل الحاشية السفلية لتحرير نص المرجع الخاص به.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// يمكننا تعيين علامة مرجعية مخصصة يستخدمها الحاشية السفلية بدلاً من رقم الفهرس الخاص بها.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// ستظل الإشارة المرجعية التي تم ضبط علم "IsAuto" عليها على "true" تعرض فهرسها الحقيقي
// حتى لو كانت الإشارات المرجعية السابقة تعرض علامات مرجعية مخصصة، فإن علامة مرجع هذه الإشارة المرجعية ستكون "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### أنظر أيضا

* class [Footnote](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
