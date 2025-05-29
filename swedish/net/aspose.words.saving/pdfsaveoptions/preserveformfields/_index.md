---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words för .NET
description: Upptäck hur PdfSaveOptions egenskap PreserveFormFields bevarar Microsoft Word-formulärfält i PDF-filer eller konverterar dem till text. Förbättra din dokumentkvalitet!
type: docs
weight: 280
url: /sv/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Anger om Microsoft Word-formulärfält ska bevaras som formulärfält i PDF eller konverteras till text. Standard är`falsk` .

```csharp
public bool PreserveFormFields { get; set; }
```

## Anmärkningar

Formulärfält i Microsoft Word inkluderar textinmatning, rullgardinsmeny och kryssrutor.

När den är inställd på`falsk` , kommer dessa fält att exporteras som text till PDF. När den är inställd på`sann`, dessa fält kommer att exporteras som PDF-formulärfält.

När du exporterar formulärfält till PDF som formulärfält kan viss formateringsförlust uppstå eftersom PDF form fields inte stöder alla funktioner i Microsoft Word-formulärfält.

Dessutom beror utdatastorleken på innehållets storlek eftersom redigerbara formulär i Microsoft Word är inline-objekt.

Redigerbara formulär är förbjudna enligt PDF/A-efterlevnad.`falsk` värdet kommer att användas automatically när du sparar till PDF/A.

Formulärfält stöds inte när man sparar till PDF/UA.`falsk` värdet kommer att användas automatiskt.

## Exempel

Visar hur man sparar ett dokument i PDF-format med hjälp av Save-metoden och PdfSaveOptions-klassen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Infoga en kombinationsruta som låter en användare välja ett alternativ från en samling strängar.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Sätt egenskapen "PreserveFormFields" till "true" för att spara formulärfält som interaktiva objekt i PDF-filen.
// Sätt egenskapen "PreserveFormFields" till "false" för att frysa alla formulärfält i dokumentet vid
// deras nuvarande värden och visa dem som vanlig text i utdata-PDF-filen.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
