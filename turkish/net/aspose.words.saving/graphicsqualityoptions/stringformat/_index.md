---
title: GraphicsQualityOptions.StringFormat
linktitle: StringFormat
articleTitle: StringFormat
second_title: .NET için Aspose.Words
description: Daha iyi görüntüleme için hizalama, üç nokta ve OpenType özellikleri de dahil olmak üzere gelişmiş metin düzeni denetimi için GraphicsQualityOptions StringFormat özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/graphicsqualityoptions/stringformat/
---
## GraphicsQualityOptions.StringFormat property

Metin düzeni bilgilerini (hizalama, yönlendirme ve sekme durakları gibi) ve görüntüleme işlemlerini (elips ekleme ve ulusal rakam değiştirme gibi) ve OpenType özelliklerini alır veya ayarlar.

```csharp
public StringFormat StringFormat { get; set; }
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
