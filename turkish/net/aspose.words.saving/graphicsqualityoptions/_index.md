---
title: GraphicsQualityOptions Class
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: .NET için Aspose.Words
description: Üstün çıktı için özelleştirilebilir seçeneklerle belge grafik kalitesini artırmak amacıyla Aspose.Words.Saving.GraphicsQualityOptions sınıfını keşfedin.
type: docs
weight: 5790
url: /tr/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Ek olarak belirtmeye izin verirGraphics kalite seçenekleri.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) belgeleme makalesi.

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
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Bileşik görüntülerin bu Grafiklere nasıl çizileceğini belirten bir değeri alır veya ayarlar. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Bu Grafiklere çizilen bileşik görüntülerin işleme kalitesini alır veya ayarlar. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Bu Grafikle ilişkili enterpolasyon modunu alır veya ayarlar. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Bu Grafik için işleme kalitesini alır veya ayarlar. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Metin düzeni bilgilerini (hizalama, yönlendirme ve sekme durakları gibi) ve görüntüleme işlemlerini (elips ekleme ve ulusal rakam değiştirme gibi) ve OpenType özelliklerini alır veya ayarlar. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | Bu Grafikle ilişkili metin için işleme modunu alır veya ayarlar. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | WrapMode'un TileFlipXY olup olmadığını belirten bir bayrak alır veya ayarlar. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
