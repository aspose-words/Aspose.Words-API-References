---
title: PdfSaveOptions.DisplayDocTitle
second_title: Aspose.Words för .NET API Referens
description: PdfSaveOptions fast egendom. En flagga som anger om fönstrets namnlist ska visa dokumenttiteln hämtad från titelposten i dokumentinformationslexikonet.
type: docs
weight: 80
url: /sv/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

En flagga som anger om fönstrets namnlist ska visa dokumenttiteln hämtad från titelposten i dokumentinformationslexikonet.

```csharp
public bool DisplayDocTitle { get; set; }
```

### Anmärkningar

Om`falsk`, bör titelraden istället visa namnet på PDF-filen som innehåller dokumentet.

Denna flagga krävs av PDF/UA-kompatibilitet.`Sann` värde kommer att användas automatiskt när du sparar till PDF/UA.

Standardvärdet är`falsk`.

### Exempel

Visar hur man visar titeln på dokumentet som namnlisten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Ställ in "DisplayDocTitle" på "true" för att få vissa PDF-läsare, som Adobe Acrobat Pro,
// för att visa värdet på dokumentets "Titel" inbyggda egenskap på fliken som hör till detta dokument.
// Ställ in "DisplayDocTitle" till "false" för att få sådana läsare att visa dokumentets filnamn.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../pdfsaveoptions/)
* hopsättning [Aspose.Words](../../../)


