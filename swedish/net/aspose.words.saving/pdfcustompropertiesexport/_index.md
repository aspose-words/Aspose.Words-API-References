---
title: Enum PdfCustomPropertiesExport
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.PdfCustomPropertiesExport uppräkning. Anger sättetCustomDocumentProperties exporteras till PDFfil.
type: docs
weight: 5420
url: /sv/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Anger sättet[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) exporteras till PDF-fil.

```csharp
public enum PdfCustomPropertiesExport
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Inga anpassade egenskaper exporteras. |
| Standard | `1` | Anpassade egenskaper exporteras som poster i /Info ordbok. |
| Metadata | `2` | Anpassade egenskaper är Metadata. |

### Exempel

Visar hur man exporterar anpassade egenskaper samtidigt som man konverterar ett dokument till PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "CustomPropertiesExport" till "PdfCustomPropertiesExport.None" för att kassera
// anpassade dokumentegenskaper när vi sparar dokumentet till .PDF.
// Ställ in egenskapen "CustomPropertiesExport" till "PdfCustomPropertiesExport.Standard"
// för att bevara anpassade egenskaper i det utgående PDF-dokumentet.
// Ställ in egenskapen "CustomPropertiesExport" till "PdfCustomPropertiesExport.Metadata"
// för att bevara anpassade egenskaper i ett XMP-paket.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


