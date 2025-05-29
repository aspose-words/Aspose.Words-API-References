---
title: XlsxSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words för .NET
description: Upptäck XlsxSaveOptions SaveFormat-egenskapen för att enkelt spara dokument i Xlsx-format, vilket säkerställer kompatibilitet och kvalitet för dina filer.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/xlsxsaveoptions/saveformat/
---
## XlsxSaveOptions.SaveFormat property

Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan endast varaXlsx .

```csharp
public override SaveFormat SaveFormat { get; set; }
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XlsxSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
