---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen PdfSaveOptions CustomPropertiesExport förbättrar dina PDF-exporter genom att styra CustomDocumentProperties för optimala resultat.
type: docs
weight: 70
url: /sv/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Hämtar eller ställer in ett värde som bestämmer hur[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) exporteras till PDF-fil.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## Anmärkningar

Standardvärdet ärNone.

Metadata värdet stöds inte vid sparning till PDF/A. Standard kommer istället att användas för PDF/A-1 och PDF/A-2 och None för PDF/A-4.

Standard värdet stöds inte vid sparning till PDF 2.0. Metadata kommer att användas istället.

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

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
