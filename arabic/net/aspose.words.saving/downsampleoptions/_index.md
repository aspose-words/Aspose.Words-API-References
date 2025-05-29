---
title: DownsampleOptions Class
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.DownsampleOptions لتخصيص عملية تقليل حجم الصورة بسهولة لتحسين جودة المستند والأداء.
type: docs
weight: 5720
url: /ar/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

يسمح بتحديد خيارات تقليل العينة.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

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
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | يحدد ما إذا كان يجب تقليل حجم الصور. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | يحدد الدقة بالبكسل لكل بوصة التي يجب تخفيض حجم الصور إليها. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | يحدد دقة العتبة بالبكسل لكل بوصة. إذا كانت دقة الصورة في المستند أقل من قيمة العتبة، لن يتم تطبيق خوارزمية تقليل العينات. تعني قيمة 0 عدم استخدام فحص العتبة وسيتم تقليل عينات جميع الصور التي يمكن تقليل حجمها. |

## أمثلة

يوضح كيفية تغيير دقة الصور في مستند PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// بشكل افتراضي، يقوم Aspose.Words بتقليص حجم جميع الصور في المستند الذي نحفظه بتنسيق PDF إلى 220 نقطة في البوصة.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// اضبط خاصية "الدقة" على "36" لتقليل دقة جميع الصور إلى 36 نقطة في البوصة.
options.DownsampleOptions.Resolution = 36;

// اضبط خاصية "ResolutionThreshold" لتطبيق تقليل العينة فقط على
// صور بدقة أعلى من 128 نقطة في البوصة.
options.DownsampleOptions.ResolutionThreshold = 128;

// سيتم تخفيض حجم الصورتين الأوليين فقط من المستند في هذه المرحلة.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
