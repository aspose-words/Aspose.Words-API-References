---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words för .NET
description: Optimera din dokumentlayout med egenskapen XpsSaveOptions UseBookFoldPrintingSettings, vilket möjliggör sömlös broschyrutskrift för förbättrad presentation.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Hämtar eller anger ett booleskt värde som anger om dokumentet ska sparas med en layout för broschyrutskrift, om det anges via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Anmärkningar

Om detta alternativ anges,[`PageSet`](../../fixedpagesaveoptions/pageset/) ignoreras vid sparning. Detta beteende matchar MS Word. Om utskriftsinställningar för bokvikning inte anges i utskriftsformatet har det här alternativet ingen effekt.

## Exempel

Visar hur man sparar ett dokument i XPS-format i form av en bokvikning.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Sätt egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
// i utdata-XPS:en på ett sätt som hjälper oss att använda den för att skapa ett häfte.
// Sätt egenskapen "UseBookFoldPrintingSettings" till "false" för att rendera XPS normalt.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Om vi renderar dokumentet som ett häfte måste vi ställa in "Flera sidor"
// egenskaper för sidinställningar-objekten för alla sektioner till "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// När vi har skrivit ut det här dokumentet kan vi göra om det till ett häfte genom att stapla sidorna
// att komma ut ur skrivaren och vika ner på mitten.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Se även

* class [XpsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
