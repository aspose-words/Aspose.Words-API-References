---
title: FootnoteOptions
second_title: Aspose.Words لمراجع .NET API
description: يوفر خيارات تتحكم في ترقيم وتحديد مواضع الحواشي السفلية في هذا المستند.
type: docs
weight: 150
url: /ar/net/aspose.words/document/footnoteoptions/
---
## Document.FootnoteOptions property

يوفر خيارات تتحكم في ترقيم وتحديد مواضع الحواشي السفلية في هذا المستند.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

### أمثلة

يوضح كيفية تحديد مكان مختلف حيث يجمع المستند ويعرض الحواشي السفلية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحاشية السفلية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// لا يتعارض مع انسياب النص الأساسي الرئيسي.  
// يؤدي إدراج حاشية سفلية إلى إضافة رمز مرجعي صغير مرتفع
// في النص الأساسي الرئيسي حيث نقوم بإدخال الحاشية السفلية.
// تقوم كل حاشية سفلية أيضًا بإنشاء إدخال في أسفل الصفحة ، يتكون من رمز
// الذي يطابق رمز المرجع في النص الأساسي الرئيسي.
// النص المرجعي الذي نمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// يمكننا استخدام خاصية "الموضع" لتحديد المكان الذي ستضع فيه الوثيقة جميع حواشيها السفلية.
// إذا قمنا بتعيين قيمة خاصية "الموضع" على "FootnotePosition.BottomOfPage" ،
// ستظهر كل حاشية سفلية في أسفل الصفحة التي تحتوي على علامتها المرجعية. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة خاصية "الموضع" على "FootnotePosition.BeneathText" ،
// ستظهر كل حاشية سفلية في نهاية نص الصفحة الذي يحتوي على علامتها المرجعية.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

يوضح كيفية تعيين رقم يبدأ عنده المستند عدد الحواشي السفلية / التعليقات الختامية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحواشي السفلية والتعليقات الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// لا يتعارض مع انسياب النص الأساسي الرئيسي. 
// يؤدي إدراج حاشية سفلية / تعليق ختامي إلى إضافة رمز مرجعي صغير مرتفع
// في النص الأساسي الرئيسي حيث نقوم بإدخال الحاشية السفلية / التعليق الختامي.
// تقوم كل حاشية سفلية / تعليق ختامي أيضًا بإنشاء إدخال يتكون من رمز
// الذي يطابق رمز المرجع في النص الأساسي الرئيسي.
// النص المرجعي الذي نمرره إلى طريقة "InsertEndnote" لمنشئ المستندات.
// تظهر إدخالات الحاشية السفلية ، افتراضيًا ، في أسفل كل صفحة تحتوي على
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

// افتراضيًا ، يكون الرمز المرجعي لكل حاشية سفلية وتعليق ختامي هو الفهرس الخاص بها
// بين جميع الحواشي السفلية / التعليقات الختامية للمستند. يحتفظ كل مستند بحسابات منفصلة
// للحواشي السفلية والتعليقات الختامية ، وكلاهما يبدأ عند 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// يمكننا استخدام خاصية "StartNumber" للحصول على المستند
// بدء عدد الحواشي السفلية أو التعليقات الختامية برقم مختلف.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

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

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
