---
title: PdfSaveOptions.UseBookFoldPrintingSettings
second_title: Aspose.Words för .NET API Referens
description: PdfSaveOptions fast egendom. Hämtar eller ställer in ett booleskt värde som indikerar om dokumentet ska sparas med en layout för häftesutskrift om det anges viaMultiplePages .
type: docs
weight: 270
url: /sv/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Hämtar eller ställer in ett booleskt värde som indikerar om dokumentet ska sparas med en layout för häftesutskrift, om det anges via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### Anmärkningar

Om detta alternativ anges,[`PageSet`](../../fixedpagesaveoptions/pageset/) ignoreras när du sparar. Det här beteendet matchar MS Word. Om inställningarna för bokvikningsutskrift inte anges i sidinställningarna har det här alternativet ingen effekt.

### Exempel

Visar hur man sparar ett dokument i PDF-format i form av en bokvikning.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
// i den utgående PDF-filen på ett sätt som hjälper oss att använda den för att göra ett häfte.
// Ställ in egenskapen "UseBookFoldPrintingSettings" till "false" för att återge PDF-filen normalt.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Om vi renderar dokumentet som ett häfte måste vi ställa in "Flera sidor"
// egenskaper för sidinställningarna för alla sektioner till "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// När vi har skrivit ut det här dokumentet på båda sidorna av sidorna kan vi vika alla sidor på mitten samtidigt,
// och innehållet kommer att radas upp på ett sätt som skapar ett häfte.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../pdfsaveoptions/)
* hopsättning [Aspose.Words](../../../)


