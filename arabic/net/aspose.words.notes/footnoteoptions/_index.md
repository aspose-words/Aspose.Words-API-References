---
title: FootnoteOptions Class
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.FootnoteOptions لترقيم الحواشي السفلية القابل للتخصيص في مستنداتك وأقسامك. حسّن وضوح مستندك اليوم!
type: docs
weight: 4970
url: /ar/net/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class

يمثل خيارات ترقيم الحواشي السفلية لمستند أو قسم.

لمعرفة المزيد، قم بزيارة[العمل مع الحواشي السفلية والختامية](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) مقالة توثيقية.

```csharp
public sealed class FootnoteOptions
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Columns](../../aspose.words.notes/footnoteoptions/columns/) { get; set; } | يحدد عدد الأعمدة التي سيتم تنسيق منطقة الحواشي السفلية بها. |
| [NumberStyle](../../aspose.words.notes/footnoteoptions/numberstyle/) { get; set; } | يحدد تنسيق الأرقام للحواشي السفلية المرقمة تلقائيًا. |
| [Position](../../aspose.words.notes/footnoteoptions/position/) { get; set; } | يحدد موضع الحواشي السفلية. |
| [RestartRule](../../aspose.words.notes/footnoteoptions/restartrule/) { get; set; } | يحدد متى يتم إعادة تشغيل الترقيم التلقائي. |
| [StartNumber](../../aspose.words.notes/footnoteoptions/startnumber/) { get; set; } | يحدد الرقم أو الحرف الأولي للحواشي السفلية المرقمة تلقائيًا. |

## أمثلة

يوضح كيفية تقسيم قسم الحاشية السفلية إلى عدد معين من الأعمدة.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

يوضح كيفية تحديد مكان مختلف لجمع المستند وعرض حواشيه السفلية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحاشية السفلية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الرئيسي.
// يؤدي إدراج حاشية سفلية إلى إضافة رمز مرجعي علوي صغير
// في نص الموضوع الرئيسي حيث نقوم بإدراج الحاشية السفلية.
// كما أن كل حاشية سفلية تنشئ إدخالاً في أسفل الصفحة، يتكون من رمز
// الذي يتطابق مع رمز المرجع في النص الرئيسي.
// نص المرجع الذي نمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستند.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// يمكننا استخدام خاصية "الموضع" لتحديد المكان الذي ستضع فيه الوثيقة جميع حواشيها السفلية.
// إذا قمنا بتعيين قيمة خاصية "Position" إلى "FootnotePosition.BottomOfPage"،
// ستظهر كل حاشية سفلية أسفل الصفحة التي تحتوي على علامتها المرجعية. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة خاصية "Position" إلى "FootnotePosition.BeneathText"،
// ستظهر كل حاشية سفلية في نهاية نص الصفحة الذي يحتوي على علامة مرجعية لها.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

يوضح كيفية تعيين رقم يبدأ عنده تعداد الحواشي السفلية/الختامية للمستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحواشي السفلية والختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الرئيسي.
// يؤدي إدراج حاشية سفلية/نهاية إلى إضافة رمز مرجعي علوي صغير
// في نص الموضوع الرئيسي حيث نقوم بإدراج الحاشية السفلية/الحاشية النهائية.
// كما أن كل حاشية سفلية/نهاية تنشئ إدخالاً يتكون من رمز
// الذي يتطابق مع رمز المرجع في النص الرئيسي.
// نص المرجع الذي نمرره إلى طريقة "InsertEndnote" الخاصة بمنشئ المستند.
// تظهر إدخالات الحواشي السفلية، بشكل افتراضي، في أسفل كل صفحة تحتوي على
//تظهر رموزها المرجعية وملاحظاتها الختامية في نهاية المستند.
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

// بشكل افتراضي، رمز المرجع لكل حاشية سفلية وحاشية نهائية هو الفهرس الخاص بها
// بين جميع حواشي المستند/الحواشي الختامية. يحتفظ كل مستند بعدد منفصل.
// للحواشي السفلية والحواشي النهائية، والتي تبدأ كلاهما عند 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// يمكننا استخدام خاصية "StartNumber" للحصول على المستند إلى
// ابدأ تعداد الحاشية السفلية أو الحاشية الختامية برقم مختلف.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

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

* property [FootnoteOptions](../../aspose.words/document/footnoteoptions/)
* property [FootnoteOptions](../../aspose.words/pagesetup/footnoteoptions/)
* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
