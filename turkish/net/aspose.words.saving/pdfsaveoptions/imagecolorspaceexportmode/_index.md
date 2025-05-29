---
title: PdfSaveOptions.ImageColorSpaceExportMode
linktitle: ImageColorSpaceExportMode
articleTitle: ImageColorSpaceExportMode
second_title: .NET için Aspose.Words
description: Çarpıcı görsel kalite ve tutarlılık için PDF'lerinizdeki görüntü rengi seçimini optimize etmek üzere PdfSaveOptions ImageColorSpaceExportMode özelliğini keşfedin.
type: docs
weight: 190
url: /tr/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

PDF belgesindeki resimler için renk alanının nasıl seçileceğini belirtir.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

## Notlar

Varsayılan değer:Auto .

EğerSimpleCmyk değer belirtildi, [`ImageCompression`](../imagecompression/) seçenek göz ardı edilir ve Belgedeki tüm resimler için Flate sıkıştırma kullanılır.

SimpleCmyk PDF/A. olarak kaydederken değer desteklenmiyorAuto Bunun yerine değer kullanılacaktır.

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

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
