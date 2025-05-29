---
title: GraphicsQualityOptions.SmoothingMode
linktitle: SmoothingMode
articleTitle: SmoothingMode
second_title: .NET için Aspose.Words
description: İşleme kalitenizi artırmak ve grafik performansınızı zahmetsizce yükseltmek için GraphicsQualityOptions SmoothingMode özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/graphicsqualityoptions/smoothingmode/
---
## GraphicsQualityOptions.SmoothingMode property

Bu Grafik için işleme kalitesini alır veya ayarlar.

```csharp
public SmoothingMode? SmoothingMode { get; set; }
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
