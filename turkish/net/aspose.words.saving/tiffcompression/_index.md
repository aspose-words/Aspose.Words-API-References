---
title: TiffCompression Enum
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: .NET için Aspose.Words
description: En iyi TIFF dosya kaydı için Aspose.Words.TiffCompression enum'unu keşfedin. Yüksek kaliteli sayfa görüntüleri için en iyi sıkıştırma türünü zahmetsizce seçin.
type: docs
weight: 6430
url: /tr/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

Sayfa görüntülerini bir TIFF dosyasına kaydederken hangi sıkıştırma türünün uygulanacağını belirtir.

```csharp
public enum TiffCompression
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Sıkıştırma yapılmayacağını belirtir. |
| Rle | `1` | RLE sıkıştırma şemasını belirtir. |
| Lzw | `2` | LZW sıkıştırma şemasını belirtir. Deflate (Zip) sıkıştırması tarafından öykünen Java'da. |
| Ccitt3 | `3` | CCITT3 sıkıştırma şemasını belirtir. |
| Ccitt4 | `4` | CCITT4 sıkıştırma şemasını belirtir. |

## Örnekler

TIFF görüntüsüne dönüştürdüğümüz bir belgeye uygulanacak sıkıştırma şemasının nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
// Kaydederken sıkıştırma yapmamak için "TiffCompression" özelliğini "TiffCompression.None" olarak ayarlayın.
// bu da çok büyük bir çıktı dosyasıyla sonuçlanabilir.
// RLE sıkıştırmasını uygulamak için "TiffCompression" özelliğini "TiffCompression.Rle" olarak ayarlayın
// LZW sıkıştırmasını uygulamak için "TiffCompression" özelliğini "TiffCompression.Lzw" olarak ayarlayın.
// CCITT3 sıkıştırmasını uygulamak için "TiffCompression" özelliğini "TiffCompression.Ccitt3" olarak ayarlayın.
// CCITT4 sıkıştırmasını uygulamak için "TiffCompression" özelliğini "TiffCompression.Ccitt4" olarak ayarlayın.
options.TiffCompression = tiffCompression;

doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
