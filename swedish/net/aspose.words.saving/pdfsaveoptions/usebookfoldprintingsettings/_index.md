---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PdfSaveOptions UseBookFoldPrintingSettings för att enkelt spara dokument i en häfteslayout för förbättrad utskriftseffektivitet.
type: docs
weight: 320
url: /sv/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Hämtar eller anger ett booleskt värde som anger om dokumentet ska sparas med en layout för broschyrutskrift, om det anges via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Anmärkningar

Om detta alternativ anges,[`PageSet`](../../fixedpagesaveoptions/pageset/) ignoreras vid sparning. Detta beteende matchar MS Word. Om utskriftsinställningar för bokvikning inte anges i utskriftsformatet har det här alternativet ingen effekt.

## Exempel

Visar hur man sparar ett dokument i PDF-format i form av en bokvikning.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Sätt egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
// i utdata-PDF:en på ett sätt som hjälper oss att använda den för att skapa ett häfte.
// Sätt egenskapen "UseBookFoldPrintingSettings" till "false" för att rendera PDF-filen normalt.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Om vi renderar dokumentet som ett häfte måste vi ställa in "Flera sidor"
// egenskaper för sidinställningar-objekten för alla sektioner till "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// När vi har skrivit ut det här dokumentet på båda sidor kan vi vika alla sidor på mitten samtidigt,
// och innehållet kommer att radas upp på ett sätt som skapar ett häfte.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
