---
title: ImageSaveOptions.GraphicsQualityOptions
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words لـ .NET
description: قم بتحسين الرسومات لديك باستخدام خاصية GraphicsQualityOptions في ImageSaveOptions، مما يتيح لك الحصول على أوضاع عرض دقيقة وجودة فائقة للحصول على صور مذهلة.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

يسمح بتحديد وضع العرض والجودة لـGraphics الكائن.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

## ملاحظات

استخدم هذه الخاصية لتجاوز إعدادات الرسومات التي يوفرها محرك Aspose.Words بشكل افتراضي.

سيتم تطبيقه فقط عند حفظ المستند بتنسيق يشبه الصورة.

## أمثلة

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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
