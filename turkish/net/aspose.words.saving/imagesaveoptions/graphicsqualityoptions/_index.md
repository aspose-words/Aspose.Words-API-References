---
title: ImageSaveOptions.GraphicsQualityOptions
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words for .NET
description: ImageSaveOptions GraphicsQualityOptions mülk. Görüntü oluşturma modunu ve kalitesini belirlemeye olanak tanır.Graphics nesne C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Görüntü oluşturma modunu ve kalitesini belirlemeye olanak tanır.Graphics nesne.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

## Notlar

Aspose.Words motoru tarafından varsayılan olarak sağlanan Grafik ayarlarını geçersiz kılmak için bu özelliği kullanın.

Yalnızca bir belge resim benzeri bir formatta kaydedildiğinde etkili olacaktır.

## Örnekler

Belgeleri görüntü formatlarına dönüştürürken işleme kalitesi seçeneklerinin nasıl ayarlanacağını gösterir.

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
