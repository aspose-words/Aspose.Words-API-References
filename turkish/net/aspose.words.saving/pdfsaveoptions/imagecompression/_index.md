---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: .NET için Aspose.Words
description: PDF'inizi PdfSaveOptions'ın ImageCompression özelliğiyle optimize edin; canlı, yüksek kaliteli görüntüler için en iyi sıkıştırma türünü seçmenize olanak tanır.
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

VarsayılanAuto.

KullanarakJpeg çıktı belgesindeki görüntülerin kalitesini kontrol etmenizi sağlar[`JpegQuality`](../jpegquality/) mülk.

KullanarakJpeg Diğer sıkıştırma türlerinin performansıyla karşılaştırıldığında en hızlı dönüştürme hızını sağlar, ancak bu durumda kayıplı JPEG sıkıştırması vardır.

KullanarakAuto Çıktı belgesindeki Jpeg kalitesini kontrol etmemize olanak sağlar[`JpegQuality`](../jpegquality/)property, ancak diğer formatlar için ham piksel verileri çıkarılır ve Flate sıkıştırmasıyla kaydedilir. Bu durum Jpeg dönüşümünden daha yavaştır ancak kayıpsızdır.

## Örnekler

PDF'ye dönüştürdüğümüz bir belgedeki tüm resimler için bir sıkıştırma türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
// "ImageCompression" özelliğini "PdfImageCompression.Auto" olarak ayarlayın
// Çıktı PDF'inde yer alan Jpeg görüntülerinin kalitesini kontrol etmek için "ImageCompression" özelliği.
// "ImageCompression" özelliğini "PdfImageCompression.Jpeg" olarak ayarlayın
// Çıktı PDF'inde yer alan tüm görsellerin kalitesini kontrol etmek için "ImageCompression" özelliği.
pdfSaveOptions.ImageCompression = pdfImageCompression;
// Görüntü kalitesinden ödün vererek sıkıştırmayı artırmak için "JpegQuality" özelliğini "10" olarak ayarlayın.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
