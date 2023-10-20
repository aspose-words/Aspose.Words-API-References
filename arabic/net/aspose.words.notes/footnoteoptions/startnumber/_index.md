---
title: FootnoteOptions.StartNumber
linktitle: StartNumber
articleTitle: StartNumber
second_title: Aspose.Words لـ .NET
description: FootnoteOptions StartNumber ملكية. يحدد رقم البداية أو الحرف لأول الحواشي السفلية المرقمة تلقائيًا في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.notes/footnoteoptions/startnumber/
---
## FootnoteOptions.StartNumber property

يحدد رقم البداية أو الحرف لأول الحواشي السفلية المرقمة تلقائيًا.

```csharp
public int StartNumber { get; set; }
```

## ملاحظات

هذه الخاصية لها تأثير فقط عندما[`RestartRule`](../restartrule/) تم ضبطه على Continuous.

## أمثلة

يوضح كيفية تعيين رقم يبدأ عنده المستند عدد الحواشي السفلية/التعليقات الختامية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحواشي السفلية والتعليقات الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الأساسي.
// يؤدي إدراج حاشية سفلية/تعليق ختامي إلى إضافة رمز مرجعي مرتفع صغير
// في النص الأساسي حيث نقوم بإدراج الحاشية السفلية/التعليق الختامي.
// تقوم كل حاشية سفلية/تعليق ختامي أيضًا بإنشاء إدخال يتكون من رمز
// الذي يطابق الرمز المرجعي في النص الأساسي.
// النص المرجعي الذي نمرره إلى طريقة "InsertEndnote" الخاصة بمنشئ المستندات.
// تظهر إدخالات الحواشي السفلية افتراضيًا في أسفل كل صفحة تحتوي على
// تظهر رموزها المرجعية والتعليقات الختامية في نهاية المستند.
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

// بشكل افتراضي، الرمز المرجعي لكل حاشية سفلية وتعليق ختامي هو الفهرس الخاص بها
// بين جميع الحواشي السفلية/التعليقات الختامية للمستند. تحتفظ كل وثيقة بأعداد منفصلة
// للحواشي السفلية والتعليقات الختامية، وكلاهما يبدأ بالرقم 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// يمكننا استخدام خاصية "StartNumber" لنقل المستند إليه
// ابدأ عدد الحاشية السفلية أو التعليقات الختامية برقم مختلف.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

### أنظر أيضا

* class [FootnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
