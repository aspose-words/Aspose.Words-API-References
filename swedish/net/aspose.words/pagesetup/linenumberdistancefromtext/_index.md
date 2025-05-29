---
title: PageSetup.LineNumberDistanceFromText
linktitle: LineNumberDistanceFromText
articleTitle: LineNumberDistanceFromText
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup LineNumberDistanceFromText för att enkelt justera avståndet mellan radnummer och dokumentets text för förbättrad läsbarhet.
type: docs
weight: 220
url: /sv/net/aspose.words/pagesetup/linenumberdistancefromtext/
---
## PageSetup.LineNumberDistanceFromText property

Hämtar eller ställer in avståndet mellan den högra kanten av radnummer och den vänstra kanten av dokumentet.

```csharp
public double LineNumberDistanceFromText { get; set; }
```

## Anmärkningar

Ställ in den här egenskapen på noll för automatiskt avstånd mellan radnummer och text i dokumentet.

## Exempel

Visar hur man aktiverar radnumrering för ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vi kan använda sektionens PageSetup-objekt för att visa siffror till vänster om sektionens textrader.
// Detta är samma beteende som ett List-objekt,
// men den täcker hela avsnittet och ändrar inte texten på något sätt.
// Vår sektion kommer att starta om numreringen på varje ny sida från 1 och visa numret,
// om det är en multipel av 3, vid 50 pt till vänster om linjen.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Radräknaren hoppar över alla stycken med flaggan "SuppressLineNumbers" inställd på "true".
// Detta stycke finns på den 15:e raden, vilket är en multipel av 3, och skulle därför normalt visa ett radnummer.
// Sektionens radräknare kommer också att ignorera denna rad, behandla nästa rad som den 15:e,
// och fortsätt räkningen från den punkten och framåt.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
