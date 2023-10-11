---
title: PdfSaveOptions.CustomPropertiesExport
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Yolu belirleyen bir değer alır veya ayarlarCustomDocumentProperties PDF dosyasına aktarılır.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Yolu belirleyen bir değer alır veya ayarlar[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) PDF dosyasına aktarılır.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

### Notlar

Varsayılan değer:None.

Metadata PDF/A'ya kaydederken değer desteklenmez. Standard bunun yerine PDF/A-1 ve PDF/A-2 ve kullanılacakNone PDF/A-4 için.

Standard PDF 2.0. 'ye kaydederken değer desteklenmiyorMetadata onun yerine kullanılacaktır.

### Örnekler

Bir belgeyi PDF'ye dönüştürürken özel özelliklerin nasıl dışa aktarılacağını gösterir.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Atmak için "CustomPropertiesExport" özelliğini "PdfCustomPropertiesExport.None" olarak ayarlayın
// belgeyi .PDF'ye kaydettiğimizde özel belge özellikleri.
// "CustomPropertiesExport" özelliğini "PdfCustomPropertiesExport.Standard" olarak ayarlayın
// çıktı PDF belgesindeki özel özellikleri korumak için.
// "CustomPropertiesExport" özelliğini "PdfCustomPropertiesExport.Metadata" olarak ayarlayın
// bir XMP paketindeki özel özellikleri korumak için.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Ayrıca bakınız

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


