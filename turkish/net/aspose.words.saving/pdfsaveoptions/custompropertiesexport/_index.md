---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: .NET için Aspose.Words
description: PdfSaveOptions CustomPropertiesExport özelliğinin, en iyi sonuçlar için CustomDocumentProperties'i kontrol ederek PDF dışa aktarımlarınızı nasıl geliştirdiğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Yolu belirleyen bir değer alır veya ayarlar[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) PDF dosyasına aktarılır.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## Notlar

Varsayılan değerNone.

Metadata PDF/A. olarak kaydederken değer desteklenmiyorStandard PDF/A-1 ve PDF/A-2 ve için bunun yerine kullanılacakNone PDF/A-4 için.

Standard PDF 2.0. olarak kaydederken değer desteklenmiyorMetadata yerine kullanılacaktır.

## Örnekler

Bir belgeyi PDF'ye dönüştürürken özel özelliklerin nasıl dışa aktarılacağını gösterir.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Atmak için "CustomPropertiesExport" özelliğini "PdfCustomPropertiesExport.None" olarak ayarlayın
// Belgeyi .PDF formatında kaydettiğimizde özel belge özellikleri.
// "CustomPropertiesExport" özelliğini "PdfCustomPropertiesExport.Standard" olarak ayarlayın
// çıktı PDF belgesinde özel özellikleri korumak için.
// "CustomPropertiesExport" özelliğini "PdfCustomPropertiesExport.Metadata" olarak ayarlayın
// XMP paketindeki özel özellikleri korumak için.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Ayrıca bakınız

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
