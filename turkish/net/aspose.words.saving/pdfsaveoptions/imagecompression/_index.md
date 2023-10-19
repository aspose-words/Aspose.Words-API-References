---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words for .NET
description: PdfSaveOptions ImageCompression mülk. Belgedeki tüm görüntüler için kullanılacak sıkıştırma türünü belirtir C#'da.
type: docs
weight: 200
url: /tr/net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

Belgedeki tüm görüntüler için kullanılacak sıkıştırma türünü belirtir.

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

## Notlar

Varsayılan:Auto.

KullanmaJpeg aracılığıyla çıktı belgesindeki görüntülerin kalitesini kontrol etmenizi sağlar.[`JpegQuality`](../jpegquality/) mülk.

KullanmaJpeg diğer sıkıştırma türlerinin performansıyla karşılaştırıldığında en hızlı dönüştürme hızını sağlar, ancak bu durumda kayıplı JPEG sıkıştırması söz konusudur.

KullanmaAuto aracılığıyla çıktı belgesindeki Jpeg kalitesinin kontrol edilmesini sağlar.[`JpegQuality`](../jpegquality/)özelliği, ancak diğer formatlar için ham piksel verileri Flate sıkıştırmasıyla çıkarılır ve kaydedilir. Bu durum Jpeg dönüşümünden daha yavaştır ancak kayıpsızdır.

## Örnekler

PDF'ye dönüştürdüğümüz bir belgedeki tüm görüntüler için sıkıştırma türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// "ImageCompression" özelliğini kullanmak için "PdfImageCompression.Auto" olarak ayarlayın.
// Çıktı PDF'sinde yer alan Jpeg görüntülerinin kalitesini kontrol etmek için "ImageCompression" özelliği.
// "ImageCompression" özelliğini kullanmak için "PdfImageCompression.Jpeg" olarak ayarlayın.
// Çıktı PDF'sinde yer alan tüm görüntülerin kalitesini kontrol etmek için "ImageCompression" özelliği.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// Görüntü kalitesinden ödün vererek sıkıştırmayı güçlendirmek için "JpegQuality" özelliğini "10" olarak ayarlayın.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
