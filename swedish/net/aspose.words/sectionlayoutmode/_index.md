---
title: Enum SectionLayoutMode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.SectionLayoutMode uppräkning. Anger layoutläget för en sektion som gör det möjligt att definiera dokumentrutnätets beteende.
type: docs
weight: 5460
url: /sv/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Anger layoutläget för en sektion som gör det möjligt att definiera dokumentrutnätets beteende.

```csharp
public enum SectionLayoutMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Default | `0` | Anger att inget dokumentrutnät ska tillämpas på innehållet i motsvarande avsnitt i dokumentet. |
| Grid | `1` | Anger att motsvarande sektion ska ha både den extra radstigningen och teckenbredden till varje rad och tecken i den för att bibehålla ett specifikt antal rader per sida och tecken per rad. Tecken kommer inte automatiskt att justeras med rutnät på skriver. |
| LineGrid | `2` | Anger att motsvarande sektion ska ha ytterligare radbredd lagt till varje rad inom it för att behålla det angivna antalet rader per sida. |
| SnapToChars | `3` | Anger att motsvarande sektion ska ha både den extra radstigningen och teckenbredden till varje rad och tecken i den för att bibehålla ett specifikt antal rader per sida och tecken per rad. Tecken kommer automatiskt att justeras med rutnät när du skriver. |

### Exempel

Visar hur man anger a för antalet tecken som varje rad kan ha.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aktivera pitching och använd den sedan för att ställa in antalet tecken per rad i det här avsnittet.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Antalet tecken beror också på storleken på teckensnittet.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

Visar hur man anger en gräns för antalet rader som varje sida kan ha.

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


