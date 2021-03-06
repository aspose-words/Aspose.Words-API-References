---
title: PdfImageCompression
second_title: Aspose.Words for .NET API Referansı
description: PDF dosyasındaki görüntülere uygulanan sıkıştırma türünü belirtir.
type: docs
weight: 5210
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
| Jpeg | `1` | Jpeg sıkıştırma. Şeffaflığı desteklemez. |

### Örnekler

PDF'ye dönüştürdüğümüz bir belgedeki tüm resimler için bir sıkıştırma türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// "ImageCompression" özelliğini kullanmak için "PdfImageCompression.Auto" olarak ayarlayın.
// Çıktı PDF'sinde yer alan Jpeg görüntülerinin kalitesini kontrol etmek için "ImageCompression" özelliği.
// "ImageCompression" özelliğini kullanmak için "PdfImageCompression.Jpeg" olarak ayarlayın.
// Çıktı PDF'sinde yer alan tüm görüntülerin kalitesini kontrol etmek için "ImageCompression" özelliği.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// Görüntü kalitesi pahasına sıkıştırmayı güçlendirmek için "JpegQuality" özelliğini "10" olarak ayarlayın.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
