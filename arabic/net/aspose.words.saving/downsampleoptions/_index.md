---
title: DownsampleOptions Class
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.DownsampleOptions فصل. يسمح بتحديد خيارات الاختزال في C#.
type: docs
weight: 4970
url: /ar/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

يسمح بتحديد خيارات الاختزال.

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
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | يحدد ما إذا كان يجب تقليل حجم الصور أم لا. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | يحدد الدقة بالبكسل لكل بوصة والتي يجب اختزال الصور إليها. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | يحدد دقة العتبة بالبكسل في البوصة. إذا كانت دقة الصورة في المستند أقل من قيمة العتبة، فلن يتم تطبيق خوارزمية الاختزال. القيمة 0 تعني عدم استخدام فحص العتبة وجميع الصور التي يمكن تقليل حجمها. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
