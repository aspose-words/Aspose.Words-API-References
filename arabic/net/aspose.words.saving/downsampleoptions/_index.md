---
title: Class DownsampleOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.DownsampleOptions فصل. يسمح بتحديد خيارات الاختزال .
type: docs
weight: 4710
url: /ar/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

يسمح بتحديد خيارات الاختزال .

```csharp
public class DownsampleOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [DownsampleOptions](downsampleoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | يحدد ما إذا كان يجب اختزال حجم الصور. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | يحدد الدقة بالبكسل في البوصة التي يجب تصغير حجم الصور إليها . |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | يحدد دقة الحد بالبكسل لكل بوصة. إذا كانت دقة صورة في المستند أقل من قيمة العتبة ، فلن يتم تطبيق خوارزمية الاختزال . القيمة 0 تعني عدم استخدام فحص الحد وجميع الصور التي يمكن تقليل حجمها يتم تصغيرها. |

### أمثلة

يوضح كيفية تغيير دقة الصور في مستند PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// بشكل افتراضي ، تختزل Aspose.Words جميع الصور في مستند نقوم بحفظه في PDF إلى 220 نقطة في البوصة.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// اضبط خاصية "Resolution" على "36" لاختزال جميع الصور إلى 36 نقطة في البوصة.
options.DownsampleOptions.Resolution = 36;

// قم بتعيين خاصية "ResolutionThreshold" لتطبيق الاختزال فقط على
// الصور بدقة أعلى من 128 نقطة في البوصة.
options.DownsampleOptions.ResolutionThreshold = 128;

// سيتم تصغير الصورتين الأوليين فقط من المستند في هذه المرحلة.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


