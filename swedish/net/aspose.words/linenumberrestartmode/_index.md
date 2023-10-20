---
title: LineNumberRestartMode Enum
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words för .NET
description: Aspose.Words.LineNumberRestartMode uppräkning. Bestämmer när automatisk radnumrering startar om i C#.
type: docs
weight: 3430
url: /sv/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

Bestämmer när automatisk radnumrering startar om.

```csharp
public enum LineNumberRestartMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| RestartPage | `0` | Radnumreringen startar om i början av varje sida. |
| RestartSection | `1` | Radnumrering startar om vid avsnittets start. |
| Continuous | `2` | Radnumrering löpande från föregående avsnitt. |

## Exempel

Visar hur man aktiverar radnumrering för en sektion.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vi kan använda sektionens PageSetup-objekt för att visa siffror till vänster om sektionens textrader.
// Detta är samma beteende som ett List-objekt,
// men det täcker hela avsnittet och ändrar inte texten på något sätt.
// Vår sektion kommer att starta om numreringen på varje ny sida från 1 och visa numret,
// om det är en multipel av 3, vid 50pt till vänster om linjen.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Radräknaren hoppar över alla stycken med flaggan "SuppressLineNumbers" inställd på "true".
// Detta stycke är på den 15:e raden, vilket är en multipel av 3, och skulle därför normalt visa ett radnummer.
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
