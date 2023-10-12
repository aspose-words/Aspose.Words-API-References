---
title: PdfSaveOptions.ImageColorSpaceExportMode
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. PDF belgesindeki görüntüler için renk alanının nasıl seçileceğini belirtir.
type: docs
weight: 190
url: /tr/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

PDF belgesindeki görüntüler için renk alanının nasıl seçileceğini belirtir.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

### Notlar

Varsayılan değer:Auto .

EğerSimpleCmyk değer belirtildi, [`ImageCompression`](../imagecompression/) seçeneği göz ardı edilir ve Belgedeki tüm görüntüler için düz sıkıştırma kullanılır.

SimpleCmyk PDF/A'ya kaydederken değer desteklenmez. Auto bunun yerine değer kullanılacaktır.

### Örnekler

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

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


