---
title: Class GraphicsQualityOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.GraphicsQualityOptions sınıf. Ek belirtmeye izin verirGraphics kalite seçenekleri.
type: docs
weight: 5040
url: /tr/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Ek belirtmeye izin verirGraphics kalite seçenekleri.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) dokümantasyon makalesi.

```csharp
public class GraphicsQualityOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [GraphicsQualityOptions](graphicsqualityoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Birleştirilmiş görüntülerin bu Grafiğe nasıl çizildiğini belirten bir değer alır veya ayarlar. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Bu Grafiğe çizilen birleştirilmiş görüntülerin işleme kalitesini alır veya ayarlar. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Bu Graphics. ile ilişkili enterpolasyon modunu alır veya ayarlar. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Bu Grafik için işleme kalitesini alır veya ayarlar. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Metin düzeni bilgilerini (hizalama, yönlendirme ve sekme durakları gibi), görüntüleme işlemlerini (üç nokta ekleme ve ulusal rakam değiştirme gibi) ve OpenType özelliklerini alır veya ayarlar. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | Bu Grafikle ilişkili metin için oluşturma modunu alır veya ayarlar. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | WrapMode'un TileFlipXY olup olmadığını belirten bir bayrağı alır veya ayarlar. |

### Örnekler

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


