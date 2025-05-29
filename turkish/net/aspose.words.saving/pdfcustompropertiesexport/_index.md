---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: .NET için Aspose.Words
description: Aspose.Words.PdfCustomPropertiesExport enumunun, en iyi sonuçlar için belge özelliklerini özelleştirerek PDF dışa aktarımlarını nasıl geliştirdiğini keşfedin.
type: docs
weight: 6210
url: /tr/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Yolu belirtir[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) PDF dosyasına aktarılır.

```csharp
public enum PdfCustomPropertiesExport
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Hiçbir özel özellik dışa aktarılmaz. |
| Standard | `1` | Özel özellikler /Info sözlüğündeki girdiler olarak dışa aktarılır. |
| Metadata | `2` | Özel özellikler Meta Verilerdir. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
