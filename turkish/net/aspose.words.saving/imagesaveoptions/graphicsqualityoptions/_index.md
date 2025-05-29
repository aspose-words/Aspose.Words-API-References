---
title: ImageSaveOptions.GraphicsQualityOptions
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: .NET için Aspose.Words
description: Grafiklerinizi ImageSaveOptions GraphicsQualityOptions özelliğiyle optimize edin, çarpıcı görseller için hassas işleme modları ve üstün kalite sağlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

İşleme modunu ve kalitesini belirtmenize olanak tanırGraphics nesne.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

## Notlar

Aspose.Words motorunun varsayılan olarak sağladığı Grafik ayarlarını geçersiz kılmak için bu özelliği kullanın.

Bu, yalnızca bir belgenin görüntü benzeri bir biçimde kaydedilmesi durumunda geçerli olacaktır.

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
