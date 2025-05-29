---
title: GraphicsQualityOptions.TextRenderingHint
linktitle: TextRenderingHint
articleTitle: TextRenderingHint
second_title: .NET için Aspose.Words
description: Grafiklerinizde optimum metin oluşturma için GraphicsQualityOptions TextRenderingHint özelliğini keşfedin. Görsel kaliteyi ve performansı bugün geliştirin!
type: docs
weight: 70
url: /tr/net/aspose.words.saving/graphicsqualityoptions/textrenderinghint/
---
## GraphicsQualityOptions.TextRenderingHint property

Bu Grafikle ilişkili metin için işleme modunu alır veya ayarlar.

```csharp
public TextRenderingHint? TextRenderingHint { get; set; }
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
