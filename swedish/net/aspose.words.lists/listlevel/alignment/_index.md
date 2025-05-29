---
title: ListLevel.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ListLevel Alignment för att enkelt anpassa justeringen av listobjekt. Förbättra ditt dokuments tydlighet och visuella attraktionskraft idag!
type: docs
weight: 10
url: /sv/net/aspose.words.lists/listlevel/alignment/
---
## ListLevel.Alignment property

Hämtar eller ställer in justeringen av det faktiska numret på listobjektet.

```csharp
public ListLevelAlignment Alignment { get; set; }
```

## Anmärkningar

Listetiketten är justerad i förhållande till[`NumberPosition`](../numberposition/) egendom.

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

* enum [ListLevelAlignment](../../listlevelalignment/)
* class [ListLevel](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
