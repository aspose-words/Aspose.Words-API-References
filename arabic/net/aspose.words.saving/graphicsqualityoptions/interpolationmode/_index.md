---
title: GraphicsQualityOptions.InterpolationMode
second_title: Aspose.Words لمراجع .NET API
description: GraphicsQualityOptions ملكية. الحصول على أو تحديد وضع الاستيفاء المرتبط بهذه الرسومات.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/graphicsqualityoptions/interpolationmode/
---
## GraphicsQualityOptions.InterpolationMode property

الحصول على أو تحديد وضع الاستيفاء المرتبط بهذه الرسومات.

```csharp
public InterpolationMode? InterpolationMode { get; set; }
```

### أمثلة

يوضح كيفية تعيين خيارات جودة العرض أثناء تحويل المستندات إلى تنسيقات صور.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions
{
    SmoothingMode = SmoothingMode.AntiAlias,
    TextRenderingHint = TextRenderingHint.ClearTypeGridFit,
    CompositingMode = CompositingMode.SourceOver,
    CompositingQuality = CompositingQuality.HighQuality,
    InterpolationMode = InterpolationMode.High,
    StringFormat = StringFormat.GenericTypographic
};

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
saveOptions.GraphicsQualityOptions = qualityOptions;

doc.Save(ArtifactsDir + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
```

### أنظر أيضا

* class [GraphicsQualityOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../graphicsqualityoptions/)
* المجسم [Aspose.Words](../../../)


