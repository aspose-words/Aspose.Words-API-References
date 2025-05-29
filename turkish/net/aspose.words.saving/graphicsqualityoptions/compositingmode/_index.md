---
title: GraphicsQualityOptions.CompositingMode
linktitle: CompositingMode
articleTitle: CompositingMode
second_title: .NET için Aspose.Words
description: Görüntülerin nasıl işlendiğini en iyi hale getirmek, grafik performansınızı ve kalitenizi artırmak için GraphicsQualityOptions CompositingMode özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/graphicsqualityoptions/compositingmode/
---
## GraphicsQualityOptions.CompositingMode property

Bileşik görüntülerin bu Grafiklere nasıl çizileceğini belirten bir değeri alır veya ayarlar.

```csharp
public CompositingMode? CompositingMode { get; set; }
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
