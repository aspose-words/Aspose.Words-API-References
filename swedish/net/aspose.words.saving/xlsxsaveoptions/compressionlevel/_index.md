---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words för .NET
description: Upptäck egenskapen XlsxSaveOptions CompressionLevel för att optimera dokumentsparandet med anpassningsbara komprimeringsinställningar för effektiv filhantering.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Anger komprimeringsnivån som används för att spara dokumentet. Standardvärdet ärNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Exempel

Visar hur man komprimerar XLSX-dokument.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum;
xlsxSaveOptions.SaveFormat = SaveFormat.Xlsx;

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Se även

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
