---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words för .NET
description: XpsSaveOptions UseBookFoldPrintingSettings fast egendom. Hämtar eller ställer in ett booleskt värde som indikerar om dokumentet ska sparas med en layout för häftesutskrift om det anges viaMultiplePages  i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Hämtar eller ställer in ett booleskt värde som indikerar om dokumentet ska sparas med en layout för häftesutskrift, om det anges via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Anmärkningar

Om detta alternativ anges,[`PageSet`](../../fixedpagesaveoptions/pageset/) ignoreras när du sparar. Det här beteendet matchar MS Word. Om inställningarna för bokvikningsutskrift inte anges i sidinställningarna har det här alternativet ingen effekt.

## Exempel

Visar hur man sparar ett dokument i XPS-format i form av en bokvikning.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Ställ in egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
// i output XPS på ett sätt som hjälper oss att använda det för att göra ett häfte.
// Ställ in egenskapen "UseBookFoldPrintingSettings" till "false" för att rendera XPS normalt.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Om vi renderar dokumentet som ett häfte måste vi ställa in "Flera sidor"
// egenskaper för sidinställningarna för alla sektioner till "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// När vi har skrivit ut det här dokumentet kan vi förvandla det till ett häfte genom att stapla sidorna
// för att komma ut ur skrivaren och fälla ner på mitten.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Se även

* class [XpsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
