---
title: PdfImageCompression Enum
linktitle: PdfImageCompression
articleTitle: PdfImageCompression
second_title: .NET için Aspose.Words
description: PDF dosyalarınızdaki görüntü sıkıştırmasını optimize etmek, kaliteyi artırmak ve dosya boyutunu zahmetsizce azaltmak için Aspose.Words.PdfImageCompression enum'unu keşfedin.
type: docs
weight: 6280
url: /tr/net/aspose.words.saving/pdfimagecompression/
---
## PdfImageCompression enumeration

PDF dosyasındaki görüntülere uygulanan sıkıştırma türünü belirtir.

```csharp
public enum PdfImageCompression
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `0` | Her görüntü için en uygun sıkıştırmayı otomatik olarak seçer. |
| Jpeg | `1` | Jpeg sıkıştırması. Şeffaflığı desteklemez. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
