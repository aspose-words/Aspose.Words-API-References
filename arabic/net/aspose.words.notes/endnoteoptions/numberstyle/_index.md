---
title: EndnoteOptions.NumberStyle
second_title: Aspose.Words لمراجع .NET API
description: EndnoteOptions ملكية. تحديد تنسيق الأرقام للتعليقات الختامية المرقمة تلقائيًا.
type: docs
weight: 10
url: /ar/net/aspose.words.notes/endnoteoptions/numberstyle/
---
## EndnoteOptions.NumberStyle property

تحديد تنسيق الأرقام للتعليقات الختامية المرقمة تلقائيًا.

```csharp
public NumberStyle NumberStyle { get; set; }
```

### ملاحظات

ليست كل أنماط الأرقام قابلة للتطبيق على هذه الخاصية. للحصول على قائمة أنماط الأرقام application ، راجع مربع الحوار "إدراج حاشية سفلية أو تعليق ختامي" في Microsoft Word. إذا قمت بتحديد نمط أرقام غير قابل للتطبيق، فسيعود Microsoft Word إلى القيمة الافتراضية.

### أمثلة

يوضح كيفية تغيير نمط الأرقام للعلامات المرجعية للحاشية السفلية/التعليق الختامي.

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
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// بشكل افتراضي، الرمز المرجعي لكل حاشية سفلية وتعليق ختامي هو الفهرس الخاص بها
// بين جميع الحواشي السفلية/التعليقات الختامية للمستند. تحتفظ كل وثيقة بأعداد منفصلة
// للحواشي السفلية والتعليقات الختامية. بشكل افتراضي، تعرض الحواشي السفلية أرقامها باستخدام الأرقام العربية،
// والحواشي الختامية تعرض أرقامها بالأرقام الرومانية الصغيرة.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// يمكننا استخدام خاصية "NumberStyle" لتطبيق أنماط ترقيم مخصصة على الحواشي السفلية والتعليقات الختامية.
// لن يؤثر هذا على الحواشي السفلية/التعليقات الختامية ذات العلامات المرجعية المخصصة.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

### أنظر أيضا

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [EndnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../endnoteoptions/)
* المجسم [Aspose.Words](../../../)


