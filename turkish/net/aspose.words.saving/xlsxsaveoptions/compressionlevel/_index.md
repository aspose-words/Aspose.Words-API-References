---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words for .NET
description: XlsxSaveOptions CompressionLevel mülk. Belgeyi kaydetmek için kullanılan sıkıştırma düzeyini belirtir. Varsayılan değerNormal  C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Belgeyi kaydetmek için kullanılan sıkıştırma düzeyini belirtir. Varsayılan değer:Normal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Örnekler

XLSX belgesinin nasıl sıkıştırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum; 

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Ayrıca bakınız

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
