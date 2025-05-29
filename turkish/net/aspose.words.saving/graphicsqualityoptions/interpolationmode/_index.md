---
title: GraphicsQualityOptions.InterpolationMode
linktitle: InterpolationMode
articleTitle: InterpolationMode
second_title: .NET için Aspose.Words
description: Grafiklerinizin enterpolasyon ayarlarını kolayca özelleştirerek gelişmiş görsel kalite elde etmek için GraphicsQualityOptions InterpolationMode özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/graphicsqualityoptions/interpolationmode/
---
## GraphicsQualityOptions.InterpolationMode property

Bu Grafikle ilişkili enterpolasyon modunu alır veya ayarlar.

```csharp
public InterpolationMode? InterpolationMode { get; set; }
```

## Örnekler

Belgeleri görüntü formatlarına dönüştürürken render kalitesi seçeneklerinin nasıl ayarlanacağını gösterir.

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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
