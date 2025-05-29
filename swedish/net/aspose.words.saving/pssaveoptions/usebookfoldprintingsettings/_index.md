---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PsSaveOptions UseBookFoldPrintingSettings för att enkelt spara dokument i en häfteslayout för förbättrad utskriftseffektivitet.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Hämtar eller anger ett booleskt värde som anger om dokumentet ska sparas med en layout för broschyrutskrift, om det anges via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Anmärkningar

Om detta alternativ anges,[`PageSet`](../../fixedpagesaveoptions/pageset/) ignoreras vid sparning. Detta beteende matchar MS Word. Om utskriftsinställningar för bokvikning inte anges i utskriftsformatet har det här alternativet ingen effekt.

## Exempel

Visar hur man sparar ett dokument i Postscript-format i form av en bokvikning.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Skapa ett "PsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till PostScript.
// Sätt egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
// i det utgående Postscript-dokumentet på ett sätt som hjälper oss att skapa ett häfte av det.
// Sätt egenskapen "UseBookFoldPrintingSettings" till "false" för att spara dokumentet normalt.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Om vi renderar dokumentet som ett häfte måste vi ställa in "Flera sidor"
// egenskaper för sidinställningar-objekten för alla sektioner till "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// När vi har skrivit ut det här dokumentet på båda sidor kan vi vika alla sidor på mitten samtidigt,
// och innehållet kommer att radas upp på ett sätt som skapar ett häfte.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Se även

* class [PsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
