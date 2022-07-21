---
title: ListLevel
second_title: Aspose.Words för .NET API Referens
description: Definierar formatering för en listnivå.
type: docs
weight: 3300
url: /sv/net/aspose.words.lists/listlevel/
---
## ListLevel class

Definierar formatering för en listnivå.

```csharp
public class ListLevel
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment) { get; set; } | Hämtar eller ställer in motiveringen för det faktiska numret för listobjektet. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat) { get; } | Hämtar det anpassade nummerformatet för denna listnivå. Till exempel: "a, ç, ĝ, ...". |
| [Font](../../aspose.words.lists/listlevel/font) { get; } | Anger teckenformatering som används för listetiketten. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata) { get; } | Returnerar bilddata för bildens kulform för den aktuella listnivån. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal) { get; set; } | Sant om nivån ändrar alla ärvda tal till arabiska, falskt om den bevarar deras talstil. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle) { get; set; } | Hämtar eller ställer in styckeformatet som är länkat till denna listnivå. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat) { get; set; } | Returnerar eller ställer in talformatet för listnivån. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition) { get; set; } | Returnerar eller ställer in positionen (i poäng) för siffran eller kulan för listnivån. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle) { get; set; } | Returnerar eller ställer in talstilen för denna listnivå. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel) { get; set; } | Ställer in eller returnerar listnivån som måste visas innan den angivna listnivån startar om numreringen. |
| [StartAt](../../aspose.words.lists/listlevel/startat) { get; set; } | Returnerar eller ställer in startnumret för denna listnivå. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition) { get; set; } | Returnerar eller ställer in tabbpositionen (i punkter) för listnivån. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition) { get; set; } | Returnerar eller ställer in positionen (i punkter) för den andra radbrytningstexten för listnivån. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter) { get; set; } | Returnerar eller ställer in tecknet som infogats efter numret för listnivån. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet)() | Skapar bildpunktform för den aktuella listnivån. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet)() | Tar bort bildpunkt för den aktuella listnivån. |
| [Equals](../../aspose.words.lists/listlevel/equals#equals)(ListLevel) | Jämför med den angivna ListLevel. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode)() | Beräknar hashkod för detta objekt. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue)(int, NumberStyle, string) | Rapporterar strängrepresentationen av[`ListLevel`](../listlevel) objekt för det angivna index för listobjektet. Parametrar anger[`NumberStyle`](../../aspose.words/numberstyle) och ett valfritt format string används närCustom anges. |

### Anmärkningar

Du skapar inte objekt av den här klassen. Objekt på listnivå skapas automatiskt när en lista skapas. Du kommer åt[`ListLevel`](../listlevel) objekt via the [`ListLevelCollection`](../listlevelcollection) samling.

Använd egenskaperna för[`ListLevel`](../listlevel) för att ange listformatering för individuella listnivåer.

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

* namnutrymme [Aspose.Words.Lists](../../aspose.words.lists)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
