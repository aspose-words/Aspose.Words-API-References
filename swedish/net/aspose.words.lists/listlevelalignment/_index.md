---
title: ListLevelAlignment Enum
linktitle: ListLevelAlignment
articleTitle: ListLevelAlignment
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Lists.ListLevelAlignment-uppräkningen för optimal listnummerering och punktjustering. Förbättra dokumentformateringen utan ansträngning!
type: docs
weight: 3960
url: /sv/net/aspose.words.lists/listlevelalignment/
---
## ListLevelAlignment enumeration

Anger justering för listnumret eller punkten.

```csharp
public enum ListLevelAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Left | `0` | Listetiketten är justerad till vänster om numrets position. |
| Center | `1` | Listetiketten är centrerad vid numrets position. |
| Right | `2` | Den här listetiketten är justerad till höger om numrets position. |

## Anmärkningar

Används som ett värde för[`Alignment`](../listlevel/alignment/) egendom.

## Exempel

Visar hur man använder anpassad listformatering på stycken när man använder DocumentBuilder.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa de två första listnivåerna.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Detta NumberFormat-värde skapar stjärnformade punktlistsymboler.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Skapa stycken och tillämpa båda listnivåerna i vår anpassade listformatering på dem.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Se även

* namnutrymme [Aspose.Words.Lists](../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../)
