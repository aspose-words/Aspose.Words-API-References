---
title: FootnoteOptions Class
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Notes.FootnoteOptions فصل. يمثل خيارات ترقيم الحواشي السفلية لمستند أو قسم في C#.
type: docs
weight: 4280
url: /ar/net/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class

يمثل خيارات ترقيم الحواشي السفلية لمستند أو قسم.

لمعرفة المزيد، قم بزيارة[العمل مع الحواشي السفلية والتعليقات الختامية](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) مقالة توثيقية.

```csharp
public sealed class FootnoteOptions
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Columns](../../aspose.words.notes/footnoteoptions/columns/) { get; set; } | يحدد عدد الأعمدة التي يتم تنسيق منطقة الحواشي السفلية بها. |
| [NumberStyle](../../aspose.words.notes/footnoteoptions/numberstyle/) { get; set; } | تحديد تنسيق الأرقام للحواشي السفلية المرقمة تلقائيًا. |
| [Position](../../aspose.words.notes/footnoteoptions/position/) { get; set; } | يحدد موضع الحواشي السفلية. |
| [RestartRule](../../aspose.words.notes/footnoteoptions/restartrule/) { get; set; } | تحديد وقت إعادة تشغيل الترقيم التلقائي. |
| [StartNumber](../../aspose.words.notes/footnoteoptions/startnumber/) { get; set; } | يحدد رقم البداية أو الحرف لأول الحواشي السفلية المرقمة تلقائيًا. |

## أمثلة

يوضح كيفية تقسيم قسم الحاشية السفلية إلى عدد معين من الأعمدة.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

يوضح كيفية تحديد مكان مختلف حيث يتم تجميع المستند وعرض حواشيه السفلية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحاشية السفلية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الأساسي.
// يؤدي إدراج حاشية سفلية إلى إضافة رمز مرجعي مرتفع صغير
// في النص الرئيسي حيث نقوم بإدراج الحاشية السفلية.
// تنشئ كل حاشية سفلية أيضًا إدخالاً في أسفل الصفحة يتكون من رمز
// الذي يطابق الرمز المرجعي في النص الأساسي.
// النص المرجعي الذي نمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// يمكننا استخدام خاصية "الموضع" لتحديد المكان الذي ستضع فيه الوثيقة جميع الحواشي السفلية.
// إذا قمنا بتعيين قيمة خاصية "الموضع" على "FootnotePosition.BottomOfPage"،
// ستظهر كل حاشية سفلية في أسفل الصفحة التي تحتوي على العلامة المرجعية الخاصة بها. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة خاصية "الموضع" على "FootnotePosition.BeneathText"،
// ستظهر كل حاشية سفلية في نهاية نص الصفحة الذي يحتوي على العلامة المرجعية الخاصة بها.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

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

* property [FootnoteOptions](../../aspose.words/document/footnoteoptions/)
* property [FootnoteOptions](../../aspose.words/pagesetup/footnoteoptions/)
* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
