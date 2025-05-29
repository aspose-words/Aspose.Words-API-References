---
title: FootnoteOptions.NumberStyle
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FootnoteOptions NumberStyle لتخصيص تنسيقات ترقيم الحواشي السفلية بسهولة لتحسين وضوح المستند واحترافيته.
type: docs
weight: 20
url: /ar/net/aspose.words.notes/footnoteoptions/numberstyle/
---
## FootnoteOptions.NumberStyle property

يحدد تنسيق الأرقام للحواشي السفلية المرقمة تلقائيًا.

```csharp
public NumberStyle NumberStyle { get; set; }
```

## ملاحظات

ليست جميع أنماط الأرقام قابلة للتطبيق على هذه الخاصية. للاطلاع على قائمة أنماط الأرقام القابلة للتطبيق ، راجع مربع حوار "إدراج حاشية سفلية أو حاشية ختامية" في Microsoft Word. إذا حددت نمط رقم غير قابل للتطبيق ، فسيعود Microsoft Word إلى القيمة الافتراضية.

## أمثلة

يوضح كيفية تغيير نمط الأرقام لعلامات مرجع الحاشية السفلية/النهاية.

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
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// بشكل افتراضي، رمز المرجع لكل حاشية سفلية وحاشية نهائية هو الفهرس الخاص بها
// بين جميع حواشي المستند/الحواشي الختامية. يحتفظ كل مستند بعدد منفصل.
// للحواشي السفلية والختامية. افتراضيًا، تعرض الحواشي السفلية أرقامها بالأرقام العربية،
// وتعرض الملاحظات الختامية أرقامها بالأرقام الرومانية الصغيرة.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// يمكننا استخدام خاصية "NumberStyle" لتطبيق أنماط الترقيم المخصصة على الحواشي السفلية والختامية.
// لن يؤثر هذا على الحواشي السفلية/النهائية التي تحتوي على علامات مرجعية مخصصة.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

### أنظر أيضا

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [FootnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
