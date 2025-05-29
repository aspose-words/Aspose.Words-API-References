---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: .NET için Aspose.Words
description: Çarpıcı görseller için PDF belgelerinizdeki resim rengi seçimini optimize etmek üzere Aspose.Words PdfImageColorSpaceExportMode enum'unu keşfedin.
type: docs
weight: 6270
url: /tr/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

PDF belgesindeki resimler için renk alanının nasıl seçileceğini belirtir.

```csharp
public enum PdfImageColorSpaceExportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `0` | Aspose.Words her görüntü için en uygun renk alanını otomatik olarak seçer. |
| SimpleCmyk | `1` | Aspose.Words, basit bir formül kullanarak RGB görüntüleri CMYK renk uzayına dönüştürür. |

## Örnekler

Bir belgeyi PDF'e aktarırken resimler için farklı bir renk alanının nasıl ayarlanacağını gösterir.

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

// Aspose.Words'ü almak için "ImageColorSpaceExportMode" özelliğini "PdfImageColorSpaceExportMode.Auto" olarak ayarlayın
// PDF'e dönüştürdüğü belgedeki resimler için renk alanını otomatik olarak seçer.
// Çoğu durumda renk alanı RGB olacaktır.
// "ImageColorSpaceExportMode" özelliğini "PdfImageColorSpaceExportMode.SimpleCmyk" olarak ayarlayın
// Kaydedilen PDF'deki tüm resimler için CMYK renk uzayını kullanmak.
// Aspose.Words ayrıca tüm resimlere Flate sıkıştırması uygulayacak ve "ImageCompression" özelliğinin değerini yok sayacaktır.
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
