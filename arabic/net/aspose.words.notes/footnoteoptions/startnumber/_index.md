---
title: FootnoteOptions.StartNumber
linktitle: StartNumber
articleTitle: StartNumber
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StartNumber في FootnoteOptions لتخصيص ترقيم الحواشي السفلية لديك، مما يعزز وضوح المستند وتنظيمه بسهولة.
type: docs
weight: 50
url: /ar/net/aspose.words.notes/footnoteoptions/startnumber/
---
## FootnoteOptions.StartNumber property

يحدد الرقم أو الحرف الأولي للحواشي السفلية المرقمة تلقائيًا.

```csharp
public int StartNumber { get; set; }
```

## ملاحظات

هذه الخاصية لها تأثير فقط عندما[`RestartRule`](../restartrule/)تم ضبطه على Continuous.

## أمثلة

يوضح كيفية تعيين رقم يبدأ عنده تعداد الحواشي السفلية/الختامية للمستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحواشي السفلية والختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الرئيسي.
// يؤدي إدراج حاشية سفلية/نهاية إلى إضافة رمز مرجعي علوي صغير
// في نص الموضوع الرئيسي حيث نقوم بإدراج الحاشية السفلية/الحاشية النهائية.
// كما أن كل حاشية سفلية/نهاية تنشئ إدخالاً يتكون من رمز
// الذي يتطابق مع رمز المرجع في النص الرئيسي.
// نص المرجع الذي نمرره إلى طريقة "InsertEndnote" الخاصة بمنشئ المستند.
// تظهر إدخالات الحواشي السفلية، بشكل افتراضي، في أسفل كل صفحة تحتوي على
//تظهر رموزها المرجعية وملاحظاتها الختامية في نهاية المستند.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// بشكل افتراضي، رمز المرجع لكل حاشية سفلية وحاشية نهائية هو الفهرس الخاص بها
// بين جميع حواشي المستند/الحواشي الختامية. يحتفظ كل مستند بعدد منفصل.
// للحواشي السفلية والحواشي النهائية، والتي تبدأ كلاهما عند 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// يمكننا استخدام خاصية "StartNumber" للحصول على المستند إلى
// ابدأ تعداد الحاشية السفلية أو الحاشية الختامية برقم مختلف.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

### أنظر أيضا

* class [FootnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
