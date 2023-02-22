---
title: PdfSaveOptions.CustomPropertiesExport
second_title: Aspose.Words för .NET API Referens
description: PdfSaveOptions fast egendom. Hämtar eller ställer in ett värde som bestämmer vägenCustomDocumentProperties exporteras till PDFfil.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Hämtar eller ställer in ett värde som bestämmer vägen[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) exporteras till PDF-fil.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

### Anmärkningar

Standardvärdet ärNone.

Metadata värde stöds inte när du sparar till PDF/A. Standard kommer att användas istället för PDF/A-1 och PDF/A-2 och None för PDF/A-4.

Standard värde stöds inte när du sparar till PDF 2.0. Metadata kommer att användas istället.

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

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../pdfsaveoptions/)
* hopsättning [Aspose.Words](../../../)


