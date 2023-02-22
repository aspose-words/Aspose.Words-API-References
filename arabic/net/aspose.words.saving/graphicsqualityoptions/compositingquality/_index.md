---
title: GraphicsQualityOptions.CompositingQuality
second_title: Aspose.Words لمراجع .NET API
description: GraphicsQualityOptions ملكية. الحصول على جودة عرض الصور المركبة المرسومة إلى هذه الرسومات أو تعيينها .
type: docs
weight: 30
url: /ar/net/aspose.words.saving/graphicsqualityoptions/compositingquality/
---
## GraphicsQualityOptions.CompositingQuality property

الحصول على جودة عرض الصور المركبة المرسومة إلى هذه الرسومات أو تعيينها .

```csharp
public CompositingQuality? CompositingQuality { get; set; }
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


