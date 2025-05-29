---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
articleTitle: DisplayDocTitle
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen PdfSaveOptions DisplayDocTitle förbättrar din PDF-upplevelse genom att visa dokumenttitlar i Windows namnlist för enkel identifiering.
type: docs
weight: 90
url: /sv/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

En flagga som anger om fönstrets titelrad ska visa dokumenttiteln hämtad från titelposten i dokumentinformationsordlistan.

```csharp
public bool DisplayDocTitle { get; set; }
```

## Anmärkningar

Om`falsk`, titelfältet bör istället visa namnet på PDF-filen som innehåller dokumentet.

Denna flagga krävs för PDF/UA-efterlevnad.`sann` Värdet kommer att användas automatiskt när sparas till PDF/UA.

Standardvärdet är`falsk`.

## Exempel

Visar hur man visar dokumentets titel som titelfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Sätt "DisplayDocTitle" till "true" för att få vissa PDF-läsare, som Adobe Acrobat Pro,
// för att visa värdet för dokumentets inbyggda egenskap "Titel" i fliken som tillhör detta dokument.
// Sätt "DisplayDocTitle" till "false" för att få sådana läsare att visa dokumentets filnamn.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
