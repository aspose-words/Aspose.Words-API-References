---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.SectionLayoutMode för att optimera avsnittslayouter och förbättra dokumentrutnätets beteende för förbättrad formateringskontroll.
type: docs
weight: 6580
url: /sv/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Anger layoutläget för ett avsnitt, vilket gör det möjligt att definiera dokumentrutnätets beteende.

```csharp
public enum SectionLayoutMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Default | `0` | Anger att inget dokumentrutnät ska tillämpas på innehållet i motsvarande avsnitt i dokumentet. |
| Grid | `1` | Anger att motsvarande avsnitt ska ha både den extra radavståndet och teckenavståndet tillagt för varje rad och tecken i det för att bibehålla ett specifikt antal rader per sida och tecken per rad. Tecken justeras inte automatiskt med rutnät vid inmatning. |
| LineGrid | `2` | Anger att motsvarande avsnitt ska ha ytterligare radavstånd tillagt för varje rad inom det. för att bibehålla det angivna antalet rader per sida. |
| SnapToChars | `3` | Anger att motsvarande avsnitt ska ha både extra radavstånd och teckenavstånd tillagt för varje rad och tecken i det för att bibehålla ett specifikt antal rader per sida och tecken per rad. Tecken justeras automatiskt med rutnätet vid inmatning. |

## Exempel

Visar hur man anger ett för antalet tecken som varje rad får innehålla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aktivera radbreddning och använd den sedan för att ange antalet tecken per rad i det här avsnittet.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Antalet tecken beror också på teckenstorleken.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

Visar hur man anger en gräns för antalet rader som varje sida får ha.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aktivera pitching och använd den sedan för att ställa in antalet rader per sida i det här avsnittet.
// En tillräckligt stor teckenstorlek kommer att trycka ner några rader till nästa sida för att undvika överlappande tecken.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
