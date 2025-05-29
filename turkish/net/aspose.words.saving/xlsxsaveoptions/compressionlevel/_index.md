---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: .NET için Aspose.Words
description: Verimli dosya yönetimi için özelleştirilebilir sıkıştırma ayarlarıyla belge kaydetmeyi optimize etmek amacıyla XlsxSaveOptions CompressionLevel özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Belgeyi kaydetmek için kullanılan sıkıştırma düzeyini belirtir. Varsayılan değerNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
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

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
