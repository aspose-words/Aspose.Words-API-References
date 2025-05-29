---
title: DownsampleOptions.ResolutionThreshold
linktitle: ResolutionThreshold
articleTitle: ResolutionThreshold
second_title: Aspose.Words لـ .NET
description: حسّن صورك باستخدام خاصية "DownsampleOptions ResolutionThreshold". تحكّم في تخفيض دقة الصورة بناءً على الدقة لتحسين الأداء والجودة.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/downsampleoptions/resolutionthreshold/
---
## DownsampleOptions.ResolutionThreshold property

يحدد دقة العتبة بالبكسل لكل بوصة. إذا كانت دقة الصورة في المستند أقل من قيمة العتبة، لن يتم تطبيق خوارزمية تقليل العينات. تعني قيمة 0 عدم استخدام فحص العتبة وسيتم تقليل عينات جميع الصور التي يمكن تقليل حجمها.

```csharp
public int ResolutionThreshold { get; set; }
```

## ملاحظات

القيمة الافتراضية هي 0.

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

* class [DownsampleOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
