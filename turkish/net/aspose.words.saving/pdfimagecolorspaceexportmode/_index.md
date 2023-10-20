---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.PdfImageColorSpaceExportMode Sıralama. PDF belgesindeki görüntüler için renk alanının nasıl seçileceğini belirtir C#'da.
type: docs
weight: 5480
url: /tr/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

PDF belgesindeki görüntüler için renk alanının nasıl seçileceğini belirtir.

```csharp
public enum PdfImageColorSpaceExportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `0` | Aspose.Words her görüntü için en uygun renk alanını otomatik olarak seçer. |
| SimpleCmyk | `1` | Aspose.Words, basit formülü kullanarak RGB görüntüleri CMYK renk uzayına dönüştürür. |

## Örnekler

Bir belgeyi PDF'ye dışa aktarırken, görüntüler için farklı bir renk alanının nasıl ayarlanacağını gösterir.

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

// Aspose.Words'ü elde etmek için "ImageColorSpaceExportMode" özelliğini "PdfImageColorSpaceExportMode.Auto" olarak ayarlayın
// PDF'ye dönüştürdüğü belgedeki görsellerin renk alanını otomatik olarak seç.
// Çoğu durumda renk alanı RGB olacaktır.
// "ImageColorSpaceExportMode" özelliğini "PdfImageColorSpaceExportMode.SimpleCmyk" olarak ayarlayın
// kayıtlı PDF'deki tüm görüntüler için CMYK renk alanını kullanmak için.
// Aspose.Words ayrıca tüm görüntülere Flate sıkıştırması uygulayacak ve "ImageCompression" özelliğinin değerini yok sayacaktır.
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
