---
title: EndnoteOptions.RestartRule
second_title: Aspose.Words لمراجع .NET API
description: EndnoteOptions ملكية. يحدد عند إعادة تشغيل الترقيم التلقائي.
type: docs
weight: 30
url: /ar/net/aspose.words.notes/endnoteoptions/restartrule/
---
## EndnoteOptions.RestartRule property

يحدد عند إعادة تشغيل الترقيم التلقائي.

```csharp
public FootnoteNumberingRule RestartRule { get; set; }
```

### ملاحظات

ليست كل القيم قابلة للتطبيق على التعليقات الختامية . للتأكد من القيم القابلة للتطبيق ، انظر[`FootnoteNumberingRule`](../../footnotenumberingrule/).

### أمثلة

يوضح كيفية إعادة تشغيل ترقيم الحواشي السفلية / التعليقات الختامية في أماكن معينة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحواشي السفلية والتعليقات الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// لا يتعارض مع انسياب النص الأساسي الرئيسي. 
// يؤدي إدراج حاشية سفلية / تعليق ختامي إلى إضافة رمز مرجعي صغير مرتفع
// في النص الأساسي الرئيسي حيث نقوم بإدخال الحاشية السفلية / التعليق الختامي.
// ينشئ كل حاشية سفلية / تعليق ختامي أيضًا إدخالًا يتكون من رمز يطابق المرجع
// رمز في النص الأساسي الرئيسي. النص المرجعي الذي نمرره إلى أسلوب "InsertEndnote" الخاص بمنشئ المستندات.
// تظهر إدخالات الحاشية السفلية ، افتراضيًا ، في أسفل كل صفحة تحتوي على
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

// افتراضيًا ، يكون الرمز المرجعي لكل حاشية سفلية وتعليق ختامي هو الفهرس الخاص بها
// بين جميع الحواشي السفلية / التعليقات الختامية للمستند. يحتفظ كل مستند بحسابات منفصلة
// للحواشي السفلية والتعليقات الختامية ولا يعيد تشغيل هذه الأعداد في أي وقت.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// يمكننا استخدام خاصية "RestartRule" لإعادة تشغيل المستند
// يتم احتساب الحاشية السفلية / التعليق الختامي في صفحة أو قسم جديد.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### أنظر أيضا

* enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* class [EndnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../endnoteoptions/)
* المجسم [Aspose.Words](../../../)


