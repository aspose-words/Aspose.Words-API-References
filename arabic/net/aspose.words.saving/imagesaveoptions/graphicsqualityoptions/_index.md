---
title: ImageSaveOptions.GraphicsQualityOptions
second_title: Aspose.Words لمراجع .NET API
description: ImageSaveOptions ملكية. يسمح بتحديد وضع العرض والجودة لـGraphics الكائن.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

يسمح بتحديد وضع العرض والجودة لـGraphics الكائن.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

### ملاحظات

استخدم هذه الخاصية لتجاوز إعدادات الرسومات التي يوفرها محرك Aspose.Words افتراضيًا.

ولن يسري مفعوله إلا عند حفظ المستند بتنسيق يشبه الصورة.

### أمثلة

يوضح كيفية تعيين خيارات جودة العرض أثناء تحويل المستندات إلى تنسيقات الصور.

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions/)
* المجسم [Aspose.Words](../../../)


