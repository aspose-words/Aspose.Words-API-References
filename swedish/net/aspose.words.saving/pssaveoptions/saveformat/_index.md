---
title: PsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PsSaveOptions SaveFormat för att enkelt ange dokumentets sparformat. Optimera ditt arbetsflöde med flexibla sparalternativ!
type: docs
weight: 20
url: /sv/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan endast varaPs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
