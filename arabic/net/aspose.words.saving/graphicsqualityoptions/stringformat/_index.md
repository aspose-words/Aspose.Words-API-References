---
title: GraphicsQualityOptions.StringFormat
second_title: Aspose.Words لمراجع .NET API
description: GraphicsQualityOptions ملكية. الحصول على معلومات تخطيط النص أو تعيينها مثل المحاذاة والاتجاه وعلامات الجدولة ومعالجات العرض مثل إدراج علامات الحذف واستبدال الأرقام الوطنية وميزات OpenType.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/graphicsqualityoptions/stringformat/
---
## GraphicsQualityOptions.StringFormat property

الحصول على معلومات تخطيط النص أو تعيينها (مثل المحاذاة والاتجاه وعلامات الجدولة) ومعالجات العرض (مثل إدراج علامات الحذف واستبدال الأرقام الوطنية) وميزات OpenType.

```csharp
public StringFormat StringFormat { get; set; }
```

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

* class [GraphicsQualityOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../graphicsqualityoptions/)
* المجسم [Aspose.Words](../../../)


