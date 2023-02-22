---
title: ImageSaveOptions.TiffCompression
second_title: Aspose.Words for .NET API Referansı
description: ImageSaveOptions mülk. Oluşturulan görüntüleri TIFF biçiminde kaydederken uygulanacak sıkıştırma türünü alır veya ayarlar.
type: docs
weight: 170
url: /tr/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Oluşturulan görüntüleri TIFF biçiminde kaydederken uygulanacak sıkıştırma türünü alır veya ayarlar.

```csharp
public TiffCompression TiffCompression { get; set; }
```

### Notlar

Yalnızca TIFF'e kaydederken etkilidir.

Varsayılan değerLzw.

### Örnekler

TIFF görüntüsüne dönüştürdüğümüz bir belgeye uygulanacak sıkıştırma şemasının nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
            // bu yöntemin belgeyi bir görüntüye dönüştürme şeklini değiştirmek için.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

            // Kaydederken sıkıştırma uygulamamak için "TiffCompression" özelliğini "TiffCompression.None" olarak ayarlayın,
            // çok büyük bir çıktı dosyasına neden olabilir.
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

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../imagesaveoptions/)
* toplantı [Aspose.Words](../../../)


