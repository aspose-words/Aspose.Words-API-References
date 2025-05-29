---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: .NET için Aspose.Words
description: TIFF resimlerinizi ImageSaveOptions TiffCompression özelliğiyle optimize ederek kaliteli sonuçlar için en iyi sıkıştırma yöntemini seçebilirsiniz.
type: docs
weight: 180
url: /tr/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

Oluşturulan görüntüleri TIFF biçimine kaydederken uygulanacak sıkıştırma türünü alır veya ayarlar.

```csharp
public TiffCompression TiffCompression { get; set; }
```

## Notlar

Sadece TIFF'e kaydederken etkilidir.

Varsayılan değer:Lzw.

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

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
