---
title: XpsSaveOptions.XpsSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: XpsSaveOptions البناء. تهيئة مثيل جديد لهذه الفئة يمكن استخدامه لحفظ document فيXps التنسيق.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

تهيئة مثيل جديد لهذه الفئة يمكن استخدامه لحفظ document فيXps التنسيق.

```csharp
public XpsSaveOptions()
```

### أمثلة

يوضح كيفية تحديد مستوى العناوين التي ستظهر في المخطط التفصيلي لمستند XPS المحفوظ.

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

// قم بإنشاء كائن "XpsSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذا الأسلوب للمستند إلى .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// سيحتوي مستند XPS الناتج على مخطط تفصيلي، وجدول محتويات يسرد العناوين في نص المستند.
// سيؤدي النقر فوق أحد الإدخالات في هذا المخطط إلى نقلنا إلى موقع العنوان الخاص به.
// قم بتعيين خاصية "HeadingsOutlineLevels" على "2" لاستبعاد جميع العناوين التي تكون مستوياتها أعلى من 2 من المخطط التفصيلي.
// لن يظهر العنوانان الأخيران اللذان أدخلناهما أعلاه.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### أنظر أيضا

* class [XpsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../xpssaveoptions/)
* المجسم [Aspose.Words](../../../)

---

## XpsSaveOptions(SaveFormat) {#constructor_1}

تهيئة مثيل جديد لهذه الفئة يمكن استخدامه لحفظ document فيXps أوOpenXps التنسيق.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

### أمثلة

يوضح كيفية حفظ مستند بتنسيق XPS على شكل طية كتاب.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// قم بإنشاء كائن "XpsSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذا الأسلوب للمستند إلى .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// اضبط خاصية "UseBookFoldPrintingSettings" على "صحيح" لترتيب المحتويات
// في مخرجات XPS بطريقة تساعدنا على استخدامها لعمل كتيب.
// قم بتعيين خاصية "UseBookFoldPrintingSettings" على "خطأ" لعرض XPS بشكل طبيعي.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// إذا كنا نعرض المستند ككتيب، فيجب علينا تعيين "الصفحات المتعددة"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// بمجرد طباعة هذه الوثيقة، يمكننا تحويلها إلى كتيب عن طريق تكديس الصفحات
// للخروج من الطابعة والطي في المنتصف.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../xpssaveoptions/)
* المجسم [Aspose.Words](../../../)


