---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: .NET için Aspose.Words
description: Belge sayfa görüntülerinde en iyi piksel biçimleri için Aspose.Words.Saving.ImagePixelFormat enum'unu keşfedin. Belge görsellerinizi zahmetsizce geliştirin!
type: docs
weight: 5970
url: /tr/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Belge sayfalarının oluşturulan görüntüleri için piksel biçimini belirtir.

```csharp
public enum ImagePixelFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Format16BppRgb555 | `0` | Piksel başına 16 bit, RGB. |
| Format16BppRgb565 | `1` | Piksel başına 16 bit, RGB. |
| Format16BppArgb1555 | `2` | Piksel başına 16 bit, ARGB. |
| Format24BppRgb | `3` | Piksel başına 24 bit, RGB. |
| Format32BppRgb | `4` | Piksel başına 32 bit, RGB. |
| Format32BppArgb | `5` | Piksel başına 32 bit, ARGB. |
| Format32BppPArgb | `6` | Piksel başına 32 bit, ARGB, önceden çarpılmış alfa. |
| Format48BppRgb | `7` | Piksel başına 48 bit, RGB. |
| Format64BppArgb | `8` | Piksel başına 64 bit, ARGB. |
| Format64BppPArgb | `9` | Piksel başına 64 bit, ARGB, önceden çarpılmış alfa. |
| Format1bppIndexed | `10` | Piksel başına 1 bit, Dizinli. |

## Örnekler

Bir belgenin görüntüye dönüştürülmesi için bit/piksel oranının nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgeyi bir resim olarak kaydettiğimizde, SaveOptions nesnesini görüntüye geçirebiliriz.
// kaydetme işleminin üreteceği görüntü için bir piksel formatı seçin.
// Çeşitli bit/piksel oranları, oluşturulan görüntünün kalitesini ve dosya boyutunu etkileyecektir.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// ImageSaveOptions örneklerini klonlayabiliriz.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
