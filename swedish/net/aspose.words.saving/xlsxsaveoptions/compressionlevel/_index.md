---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words för .NET
description: XlsxSaveOptions CompressionLevel fast egendom. Anger komprimeringsnivån som används för att spara dokument. Standardvärdet ärNormal  i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Anger komprimeringsnivån som används för att spara dokument. Standardvärdet ärNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Exempel

Visar hur man komprimerar XLSX-dokument.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum; 

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Se även

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
