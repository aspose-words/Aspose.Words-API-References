---
title: Enum TiffCompression
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.TiffCompression Sıralama. Sayfa görüntülerini bir TIFF dosyasına kaydederken ne tür sıkıştırmanın uygulanacağını belirtir.
type: docs
weight: 5630
url: /tr/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

Sayfa görüntülerini bir TIFF dosyasına kaydederken ne tür sıkıştırmanın uygulanacağını belirtir.

```csharp
public enum TiffCompression
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Sıkıştırma olmadığını belirtir. |
| Rle | `1` | RLE sıkıştırma şemasını belirtir. |
| Lzw | `2` | LZW sıkıştırma şemasını belirtir. Java'da Deflate (Zip) sıkıştırması ile öykünülür. |
| Ccitt3 | `3` | CCITT3 sıkıştırma şemasını belirtir. |
| Ccitt4 | `4` | CCITT4 sıkıştırma şemasını belirtir. |

### Örnekler

TIFF görüntüsüne dönüştürdüğümüz bir belgeye uygulanacak sıkıştırma şemasının nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Belgenin "Save" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
            // bu yöntemin belgeyi bir görüntüye dönüştürme biçimini değiştirmek için.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

            // Kaydetme sırasında sıkıştırma uygulamamak için "TiffCompression" özelliğini "TiffCompression.None" olarak ayarlayın,
            // bu çok büyük bir çıktı dosyasıyla sonuçlanabilir.
            // RLE sıkıştırmasını uygulamak için "TiffCompression" özelliğini "TiffCompression.Rle" olarak ayarlayın
            // LZW sıkıştırmasını uygulamak için "TiffCompression" özelliğini "TiffCompression.Lzw" olarak ayarlayın.
            // CCITT3 sıkıştırmasını uygulamak için "TiffCompression" özelliğini "TiffCompression.Ccitt3" olarak ayarlayın.
            // CCITT4 sıkıştırmasını uygulamak için "TiffCompression" özelliğini "TiffCompression.Ccitt4" olarak ayarlayın.
            options.TiffCompression = tiffCompression;

            doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);

            switch (tiffCompression)
            {
                case TiffCompression.None:
                    Assert.That(3000000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Rle:
#if NET5_0_OR_GREATER
                    Assert.That(6000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#else
                    Assert.That(600000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#endif
                    break;
                case TiffCompression.Lzw:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt3:
                    Assert.That(90000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt4:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
            }
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


