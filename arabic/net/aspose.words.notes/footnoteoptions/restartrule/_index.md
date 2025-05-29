---
title: FootnoteOptions.RestartRule
linktitle: RestartRule
articleTitle: RestartRule
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FootnoteOptions RestartRule للتحكم في إعادة ضبط الترقيم تلقائيًا، مما يُحسّن تنظيم المستندات ووضوحها. حسّن سير عملك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.notes/footnoteoptions/restartrule/
---
## FootnoteOptions.RestartRule property

يحدد متى يتم إعادة تشغيل الترقيم التلقائي.

```csharp
public FootnoteNumberingRule RestartRule { get; set; }
```

## أمثلة

يوضح كيفية إعادة تشغيل ترقيم الحواشي السفلية/الختامية في أماكن معينة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحواشي السفلية والختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الرئيسي.
// يؤدي إدراج حاشية سفلية/نهاية إلى إضافة رمز مرجعي علوي صغير
// في نص الموضوع الرئيسي حيث نقوم بإدراج الحاشية السفلية/الحاشية النهائية.
// كما أن كل حاشية سفلية/نهاية تنشئ إدخالاً يتكون من رمز يتطابق مع المرجع
// رمز في النص الرئيسي. النص المرجعي الذي نُمرر إلى دالة "InsertEndnote" في مُنشئ المستندات.
// تظهر إدخالات الحواشي السفلية، بشكل افتراضي، في أسفل كل صفحة تحتوي على
//تظهر رموزها المرجعية وملاحظاتها الختامية في نهاية المستند.
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

// بشكل افتراضي، رمز المرجع لكل حاشية سفلية وحاشية نهائية هو الفهرس الخاص بها
// بين جميع حواشي المستند/الحواشي الختامية. يحتفظ كل مستند بعدد منفصل.
// للحواشي السفلية والختامية ولا يتم إعادة تشغيل هذه العد في أي نقطة.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// يمكننا استخدام خاصية "RestartRule" لإعادة تشغيل المستند
// يتم احتساب الحاشية السفلية/الحاشية النهائية في الصفحة أو القسم الجديد.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### أنظر أيضا

* enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* class [FootnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
