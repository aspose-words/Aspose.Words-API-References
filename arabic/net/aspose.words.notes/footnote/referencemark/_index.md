---
title: Footnote.ReferenceMark
linktitle: ReferenceMark
articleTitle: ReferenceMark
second_title: Aspose.Words لـ .NET
description: خصّص حواشيك السفلية باستخدام خاصية ReferenceMark. حدّد بسهولة علامات فريدة للوضوح والتنظيم في مستنداتك. حسّن سهولة القراءة اليوم!
type: docs
weight: 60
url: /ar/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

يحصل على/يعين علامة مرجعية مخصصة لاستخدامها في هذه الحاشية السفلية. القيمة الافتراضية هي**سلسلة فارغة** (Empty )، مما يعني أنه يتم استخدام الحواشي المرقمة تلقائيًا.

```csharp
public string ReferenceMark { get; set; }
```

## ملاحظات

إذا تم تعيين هذه الخاصية على**سلسلة فارغة** (Empty ) أو`باطل` ، ثم[`IsAuto`](../isauto/) سيتم تعيين الخاصية تلقائيًا إلى`حقيقي` ، إذا تم ضبطه على أي شيء آخر،[`IsAuto`](../isauto/) سيتم ضبطه على`خطأ شنيع` .

تنسيق RTF يمكنه تخزين رمز واحد فقط كعلامة مرجعية مخصصة، لذلك عند التصدير سيتم كتابة الرمز الأول فقط وسيتم تجاهل الرموز الأخرى.

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
