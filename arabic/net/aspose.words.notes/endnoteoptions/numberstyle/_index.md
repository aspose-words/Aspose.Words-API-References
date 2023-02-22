---
title: EndnoteOptions.NumberStyle
second_title: Aspose.Words لمراجع .NET API
description: EndnoteOptions ملكية. يحدد تنسيق الأرقام للتعليقات الختامية المرقمة تلقائيًا.
type: docs
weight: 10
url: /ar/net/aspose.words.notes/endnoteoptions/numberstyle/
---
## EndnoteOptions.NumberStyle property

يحدد تنسيق الأرقام للتعليقات الختامية المرقمة تلقائيًا.

```csharp
public NumberStyle NumberStyle { get; set; }
```

### ملاحظات

ليست كل أنماط الأرقام قابلة للتطبيق على هذه الخاصية. للحصول على قائمة أنماط الأرقام القابلة للتطبيق ، راجع مربع الحوار "إدراج حاشية سفلية أو تعليق ختامي" في Microsoft Word. إذا حددت نمط رقم غير قابل للتطبيق ، فسيعود Microsoft Word إلى القيمة الافتراضية.

### أمثلة

يوضح كيفية تغيير نمط عدد العلامات المرجعية للحواشي السفلية / التعليقات الختامية.

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
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// افتراضيًا ، يكون الرمز المرجعي لكل حاشية سفلية وتعليق ختامي هو الفهرس الخاص بها
// بين جميع الحواشي السفلية / التعليقات الختامية للمستند. يحتفظ كل مستند بحسابات منفصلة
// للهوامش والتعليقات الختامية. بشكل افتراضي ، تعرض الحواشي السفلية أرقامها باستخدام الأرقام العربية ،
// والتعليقات الختامية تعرض أرقامها بأرقام رومانية صغيرة.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// يمكننا استخدام خاصية "NumberStyle" لتطبيق أنماط ترقيم مخصصة على الحواشي السفلية والتعليقات الختامية.
// لن يؤثر هذا على الحواشي السفلية / التعليقات الختامية بعلامات مرجعية مخصصة.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

### أنظر أيضا

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [EndnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../endnoteoptions/)
* المجسم [Aspose.Words](../../../)


