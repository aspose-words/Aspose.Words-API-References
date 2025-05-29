---
title: XlsxSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: Dosyalarınızın uyumluluğunu ve kalitesini garanti altına alarak, belgeleri Xlsx formatında zahmetsizce kaydetmek için XlsxSaveOptions SaveFormat özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/xlsxsaveoptions/saveformat/
---
## XlsxSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaXlsx .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Örnekler

XLSX belgesinin nasıl sıkıştırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum;
xlsxSaveOptions.SaveFormat = SaveFormat.Xlsx;

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XlsxSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
