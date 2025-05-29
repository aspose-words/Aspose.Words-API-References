---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.PdfCustomPropertiesExport-enum förbättrar PDF-exporter genom att anpassa dokumentegenskaper för optimala resultat.
type: docs
weight: 6210
url: /sv/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Anger hur[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) exporteras till PDF-fil.

```csharp
public enum PdfCustomPropertiesExport
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Inga anpassade egenskaper exporteras. |
| Standard | `1` | Anpassade egenskaper exporteras som poster i /Info-ordboken. |
| Metadata | `2` | Anpassade egenskaper är metadata. |

## Exempel

Visar hur man exporterar anpassade egenskaper när man konverterar ett dokument till PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Sätt egenskapen "CustomPropertiesExport" till "PdfCustomPropertiesExport.None" för att ignorera
// anpassade dokumentegenskaper när vi sparar dokumentet till .PDF.
// Ställ in egenskapen "CustomPropertiesExport" till "PdfCustomPropertiesExport.Standard"
// för att bevara anpassade egenskaper i PDF-dokumentet som utdata.
// Ställ in egenskapen "CustomPropertiesExport" till "PdfCustomPropertiesExport.Metadata"
// för att bevara anpassade egenskaper i ett XMP-paket.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
