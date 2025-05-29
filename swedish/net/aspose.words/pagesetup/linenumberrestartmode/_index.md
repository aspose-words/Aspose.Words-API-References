---
title: PageSetup.LineNumberRestartMode
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup LineNumberRestartMode för att styra radnumrering – välj mellan att starta om vid nya sidor eller kontinuerlig numrering för sömlösa dokument.
type: docs
weight: 230
url: /sv/net/aspose.words/pagesetup/linenumberrestartmode/
---
## PageSetup.LineNumberRestartMode property

Hämtar eller anger hur radnumreringen körs, det vill säga om den börjar om i början av en ny sida eller ett nytt avsnitt eller körs kontinuerligt.

```csharp
public LineNumberRestartMode LineNumberRestartMode { get; set; }
```

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

* enum [LineNumberRestartMode](../../linenumberrestartmode/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
