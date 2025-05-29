---
title: PdfSaveOptions.ExportDocumentStructure
linktitle: ExportDocumentStructure
articleTitle: ExportDocumentStructure
second_title: Aspose.Words för .NET
description: Kontrollera ditt dokuments exportstruktur med PdfSaveOptions. Hantera enkelt inställningar för optimal PDF-utdata och förbättra ditt arbetsflödes effektivitet.
type: docs
weight: 140
url: /sv/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Hämtar eller anger ett värde som avgör om dokumentstrukturen ska exporteras eller inte.

```csharp
public bool ExportDocumentStructure { get; set; }
```

## Anmärkningar

Detta värde ignoreras när man sparar till PDF/A-1a, PDF/A-2a och PDF/UA-1 eftersom dokumentstruktur krävs för denna överensstämmelse.

Observera att export av dokumentstrukturen ökar minnesförbrukningen avsevärt, särskilt för stora dokument.

## Exempel

Visar hur man bevarar dokumentstrukturelement, vilket kan hjälpa till att programmatiskt tolka vårt dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Sätt egenskapen "ExportDocumentStructure" till "true" för att göra dokumentstrukturen, såsom taggar, tillgängliga via
// Navigeringsfönstret "Innehåll" i Adobe Acrobat på bekostnad av ökad filstorlek.
// Sätt egenskapen "ExportDocumentStructure" till "false" för att inte exportera dokumentstrukturen.
options.ExportDocumentStructure = exportDocumentStructure;

// Anta att vi exporterar dokumentstrukturen medan vi sparar detta dokument. I så fall,
// vi kan öppna den med Adobe Acrobat och hitta taggar för element som rubriken
// och nästa stycke via "Visa" -> "Visa/Dölj" -> "Navigeringsrutor" -> "Taggar".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
