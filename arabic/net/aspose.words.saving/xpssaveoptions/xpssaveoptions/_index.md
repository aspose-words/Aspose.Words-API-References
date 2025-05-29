---
title: XpsSaveOptions
linktitle: XpsSaveOptions
articleTitle: XpsSaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف منشئ XpsSaveOptions لإنشاء حالات لحفظ المستندات بتنسيق XPS بسهولة، مما يعزز كفاءة إدارة المستندات لديك.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ document فيXps تنسيق.

```csharp
public XpsSaveOptions()
```

## أمثلة

يوضح كيفية تحديد مستوى العناوين التي ستظهر في مخطط مستند XPS المحفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل العناوين التي يمكن أن تكون بمثابة إدخالات جدول المحتويات للمستويات 1، 2، ثم 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// قم بإنشاء كائن "XpsSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// سيحتوي مستند XPS الناتج على مخطط تفصيلي، وهو جدول محتويات يسرد العناوين الموجودة في نص المستند.
// النقر على إدخال في هذا المخطط سيأخذنا إلى موقع العنوان الخاص به.
// قم بضبط خاصية "HeadingsOutlineLevels" على "2" لاستبعاد جميع العناوين التي تكون مستوياتها أعلى من 2 من المخطط التفصيلي.
// لن يظهر آخر عنوانين قمنا بإدخالهما أعلاه.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### أنظر أيضا

* class [XpsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)

---

## XpsSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ document فيXps أوOpenXps تنسيق.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

## أمثلة

يوضح كيفية حفظ مستند بتنسيق XPS في شكل كتاب مطوي.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// قم بإنشاء كائن "XpsSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// اضبط خاصية "UseBookFoldPrintingSettings" على "true" لترتيب المحتويات
// في إخراج XPS بطريقة تساعدنا على استخدامه لإنشاء كتيب.
// قم بضبط خاصية "UseBookFoldPrintingSettings" على "false" لعرض XPS بشكل طبيعي.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// إذا كنا نعرض المستند ككتيب، فيجب علينا تعيين "صفحات متعددة"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// بمجرد طباعة هذه الوثيقة، يمكننا تحويلها إلى كتيب عن طريق تكديس الصفحات
// للخروج من الطابعة وطيها من المنتصف.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
