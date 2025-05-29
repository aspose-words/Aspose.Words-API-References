---
title: LineNumberRestartMode Enum
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.LineNumberRestartMode-enumreringen för att styra automatiska återställningar av radnumrering för förbättrad dokumentformatering och tydlighet.
type: docs
weight: 3880
url: /sv/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

Avgör när automatisk radnumrering startar om.

```csharp
public enum LineNumberRestartMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| RestartPage | `0` | Radnumreringen börjar om i början av varje sida. |
| RestartSection | `1` | Radnumreringen börjar om vid avsnittets början. |
| Continuous | `2` | Radnumrering i fortsättning från föregående avsnitt. |

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

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
