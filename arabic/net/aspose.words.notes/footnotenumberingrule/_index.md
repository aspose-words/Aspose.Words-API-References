---
title: Enum FootnoteNumberingRule
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Notes.FootnoteNumberingRule تعداد. تحديد متى يتم إعادة تشغيل ترقيم الحواشي السفلية أو التعليقات الختامية تلقائيًا.
type: docs
weight: 4270
url: /ar/net/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enumeration

تحديد متى يتم إعادة تشغيل ترقيم الحواشي السفلية أو التعليقات الختامية تلقائيًا.

```csharp
public enum FootnoteNumberingRule
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Continuous | `0` | الترقيم المستمر في جميع أنحاء الوثيقة. |
| RestartSection | `1` | تتم إعادة تشغيل الترقيم عند كل قسم. |
| RestartPage | `2` | تتم إعادة تشغيل الترقيم في كل صفحة. صالح للحواشي السفلية فقط. |
| Default | `0` | يساويContinuous . |

### أمثلة

يوضح كيفية إعادة تشغيل ترقيم الحواشي السفلية/التعليقات الختامية في أماكن معينة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحواشي السفلية والتعليقات الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الأساسي.
// يؤدي إدراج حاشية سفلية/تعليق ختامي إلى إضافة رمز مرجعي مرتفع صغير
// في النص الأساسي حيث نقوم بإدراج الحاشية السفلية/التعليق الختامي.
// تقوم كل حاشية سفلية/تعليق ختامي أيضًا بإنشاء إدخال يتكون من رمز يطابق المرجع
// الرمز في النص الأساسي. النص المرجعي الذي نمرره إلى طريقة "InsertEndnote" الخاصة بمنشئ المستندات.
// تظهر إدخالات الحواشي السفلية افتراضيًا في أسفل كل صفحة تحتوي على
// تظهر رموزها المرجعية والتعليقات الختامية في نهاية المستند.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// بشكل افتراضي، الرمز المرجعي لكل حاشية سفلية وتعليق ختامي هو الفهرس الخاص بها
// بين جميع الحواشي السفلية/التعليقات الختامية للمستند. تحتفظ كل وثيقة بأعداد منفصلة
// للحواشي السفلية والتعليقات الختامية ولا يعيد تشغيل هذه الأعداد في أي وقت.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// يمكننا استخدام خاصية "RestartRule" لإعادة تشغيل المستند
// يتم احتساب الحاشية السفلية/التعليق الختامي في صفحة أو قسم جديد.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### أنظر أيضا

* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)
* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)


