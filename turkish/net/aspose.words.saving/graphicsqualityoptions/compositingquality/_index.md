---
title: GraphicsQualityOptions.CompositingQuality
second_title: Aspose.Words for .NET API Referansı
description: GraphicsQualityOptions mülk. Bu Grafiklere çizilen birleştirilmiş görüntülerin işleme kalitesini alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/graphicsqualityoptions/compositingquality/
---
## GraphicsQualityOptions.CompositingQuality property

Bu Grafiklere çizilen birleştirilmiş görüntülerin işleme kalitesini alır veya ayarlar.

```csharp
public CompositingQuality? CompositingQuality { get; set; }
```

### Örnekler

Belgeleri görüntü biçimlerine dönüştürürken işleme kalitesi seçeneklerinin nasıl ayarlanacağını gösterir.

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

### Ayrıca bakınız

* class [GraphicsQualityOptions](../)
* ad alanı [Aspose.Words.Saving](../../graphicsqualityoptions/)
* toplantı [Aspose.Words](../../../)


