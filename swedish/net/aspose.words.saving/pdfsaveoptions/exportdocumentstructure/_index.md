---
title: PdfSaveOptions.ExportDocumentStructure
second_title: Aspose.Words för .NET API Referens
description: PdfSaveOptions fast egendom. Hämtar eller ställer in ett värde som avgör om dokumentstruktur ska exporteras eller inte.
type: docs
weight: 120
url: /sv/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Hämtar eller ställer in ett värde som avgör om dokumentstruktur ska exporteras eller inte.

```csharp
public bool ExportDocumentStructure { get; set; }
```

### Anmärkningar

Detta värde ignoreras när du sparar till PDF/A-1a, PDF/A-2a och PDF/UA-1 eftersom dokumentstruktur krävs för denna överensstämmelse.

Observera att export av dokumentstrukturen avsevärt ökar minnesförbrukningen, särskilt för de stora dokumenten.

### Exempel

Visar hur man bevarar dokumentstrukturelement, vilket kan hjälpa till att programmässigt tolka vårt dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "ExportDocumentStructure" till "true" för att göra dokumentstrukturen, sådana taggar, tillgänglig via
// Navigeringsfönstret "Innehåll" i Adobe Acrobat till priset av ökad filstorlek.
// Ställ in egenskapen "ExportDocumentStructure" till "false" för att inte exportera dokumentstrukturen.
options.ExportDocumentStructure = exportDocumentStructure;

// Antag att vi exporterar dokumentstruktur medan vi sparar detta dokument. Isåfall,
// vi kan öppna den med Adobe Acrobat och hitta taggar för element som rubriken
// och nästa stycke via "Visa" -> "Visa/Dölj" -> "Navigeringsrutor" -> "Taggar".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../pdfsaveoptions/)
* hopsättning [Aspose.Words](../../../)


