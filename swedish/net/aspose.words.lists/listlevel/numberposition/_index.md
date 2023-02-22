---
title: ListLevel.NumberPosition
second_title: Aspose.Words för .NET API Referens
description: ListLevel fast egendom. Returnerar eller ställer in positionen i poäng för siffran eller kulan för listnivån.
type: docs
weight: 80
url: /sv/net/aspose.words.lists/listlevel/numberposition/
---
## ListLevel.NumberPosition property

Returnerar eller ställer in positionen (i poäng) för siffran eller kulan för listnivån.

```csharp
public double NumberPosition { get; set; }
```

### Anmärkningar

`NumberPosition` motsvarar LeftIndent plus FirstLineIndent i stycket.

### Exempel

Visar hur du använder anpassad listformatering på stycken när du använder DocumentBuilder.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa kapslade listor genom att öka indragsnivån. 
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares "ListFormat"-egenskap. 
// Varje stycke som vi lägger till mellan en listas början och slutet kommer att bli ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa de två första av listnivåerna.
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

* class [ListLevel](../)
* namnutrymme [Aspose.Words.Lists](../../listlevel/)
* hopsättning [Aspose.Words](../../../)


