---
title: DownsampleOptions.Resolution
second_title: Aspose.Words لمراجع .NET API
description: DownsampleOptions ملكية. يحدد الدقة بالبكسل لكل بوصة والتي يجب اختزال الصور إليها.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

يحدد الدقة بالبكسل لكل بوصة والتي يجب اختزال الصور إليها.

```csharp
public int Resolution { get; set; }
```

### ملاحظات

القيمة الافتراضية هي 220 نقطة في البوصة.

### أمثلة

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
* مساحة الاسم [Aspose.Words.Saving](../../downsampleoptions/)
* المجسم [Aspose.Words](../../../)


