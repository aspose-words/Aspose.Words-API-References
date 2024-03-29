---
title: DownsampleOptions.ResolutionThreshold
linktitle: ResolutionThreshold
articleTitle: ResolutionThreshold
second_title: Aspose.Words لـ .NET
description: DownsampleOptions ResolutionThreshold ملكية. يحدد دقة العتبة بالبكسل في البوصة. إذا كانت دقة الصورة في المستند أقل من قيمة العتبة فلن يتم تطبيق خوارزمية الاختزال. القيمة 0 تعني عدم استخدام فحص العتبة وجميع الصور التي يمكن تقليل حجمها في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/downsampleoptions/resolutionthreshold/
---
## DownsampleOptions.ResolutionThreshold property

يحدد دقة العتبة بالبكسل في البوصة. إذا كانت دقة الصورة في المستند أقل من قيمة العتبة، فلن يتم تطبيق خوارزمية الاختزال. القيمة 0 تعني عدم استخدام فحص العتبة وجميع الصور التي يمكن تقليل حجمها.

```csharp
public int ResolutionThreshold { get; set; }
```

## ملاحظات

القيمة الافتراضية هي 0.

## أمثلة

يوضح كيفية تغيير دقة الصور في مستند PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// بشكل افتراضي، يقوم Aspose.Words باختزال جميع الصور في المستند الذي نحفظه إلى PDF إلى 220 نقطة في البوصة.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// اضبط خاصية "الدقة" على "36" لاختزال جميع الصور إلى 36 نقطة في البوصة.
options.DownsampleOptions.Resolution = 36;

// قم بتعيين خاصية "ResolutionThreshold" لتطبيق الاختزال عليها فقط
// الصور بدقة أعلى من 128 نقطة في البوصة.
options.DownsampleOptions.ResolutionThreshold = 128;

// سيتم تصغير حجم الصورتين الأوليين فقط من المستند في هذه المرحلة.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### أنظر أيضا

* class [DownsampleOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
