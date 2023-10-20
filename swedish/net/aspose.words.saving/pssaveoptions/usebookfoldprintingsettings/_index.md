---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words för .NET
description: PsSaveOptions UseBookFoldPrintingSettings fast egendom. Hämtar eller ställer in ett booleskt värde som indikerar om dokumentet ska sparas med en layout för häftesutskrift om det anges viaMultiplePages  i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Hämtar eller ställer in ett booleskt värde som indikerar om dokumentet ska sparas med en layout för häftesutskrift, om det anges via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Anmärkningar

Om detta alternativ anges,[`PageSet`](../../fixedpagesaveoptions/pageset/) ignoreras när du sparar. Det här beteendet matchar MS Word. Om inställningarna för bokvikningsutskrift inte anges i sidinställningarna har det här alternativet ingen effekt.

## Exempel

Visar hur man sparar ett dokument i Postscript-format i form av en bokvikning.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Skapa ett "PsSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till PostScript.
// Ställ in egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
// i det utgående Postscript-dokumentet på ett sätt som hjälper oss att göra ett häfte av det.
// Ställ in egenskapen "UseBookFoldPrintingSettings" till "false" för att spara dokumentet normalt.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Om vi renderar dokumentet som ett häfte måste vi ställa in "Flera sidor"
// egenskaper för sidinställningarna för alla sektioner till "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// När vi har skrivit ut det här dokumentet på båda sidorna av sidorna kan vi vika alla sidor på mitten samtidigt,
// och innehållet kommer att radas upp på ett sätt som skapar ett häfte.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Se även

* class [PsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
