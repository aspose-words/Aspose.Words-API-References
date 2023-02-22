---
title: Enum PdfImageColorSpaceExportMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.PdfImageColorSpaceExportMode Sıralama. PDF belgesindeki resimler için renk uzayının nasıl seçileceğini belirtir.
type: docs
weight: 5200
url: /tr/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

PDF belgesindeki resimler için renk uzayının nasıl seçileceğini belirtir.

```csharp
public enum PdfImageColorSpaceExportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `0` | Aspose.Words, her görüntü için en uygun renk alanını otomatik olarak seçer. |
| SimpleCmyk | `1` | Aspose.Words, basit formül kullanarak RGB görüntüleri CMYK renk uzayına dönüştürür. |

### Örnekler

PDF'ye dışa aktarırken bir belgedeki görüntüler için nasıl farklı bir renk uzayı ayarlanacağını gösterir.

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

// Aspose.Words'ü almak için "ImageColorSpaceExportMode" özelliğini "PdfImageColorSpaceExportMode.Auto" olarak ayarlayın
// PDF'ye dönüştürdüğü belgedeki resimler için renk uzayını otomatik olarak seç.
// Çoğu durumda renk uzayı RGB olacaktır.
// "ImageColorSpaceExportMode" özelliğini "PdfImageColorSpaceExportMode.SimpleCmyk" olarak ayarlayın
// kaydedilen PDF'deki tüm resimler için CMYK renk alanını kullanmak için.
// Aspose.Words ayrıca tüm görüntülere Flate sıkıştırması uygulayacak ve "ImageCompression" özelliğinin değerini yok sayacaktır.
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


