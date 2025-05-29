---
title: FootnoteNumberingRule Enum
linktitle: FootnoteNumberingRule
articleTitle: FootnoteNumberingRule
second_title: Aspose.Words لـ .NET
description: اكتشف قاعدة ترقيم الحواشي السفلية والختامية في Aspose.Words للتحكم التلقائي في ترقيم الحواشي السفلية والختامية. حسّن تنسيق مستندك بسهولة!
type: docs
weight: 4960
url: /ar/net/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enumeration

يحدد متى يتم إعادة تشغيل الترقيم التلقائي للحواشي السفلية أو النهائية.

```csharp
public enum FootnoteNumberingRule
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Continuous | `0` | الترقيم مستمر في جميع أنحاء المستند. |
| RestartSection | `1` | يتم إعادة تشغيل الترقيم في كل قسم. |
| RestartPage | `2` | يُعاد ترقيم الصفحة عند كل صفحة. صالح للحواشي السفلية فقط. |
| Default | `0` | يساويContinuous . |

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

* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)
* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
