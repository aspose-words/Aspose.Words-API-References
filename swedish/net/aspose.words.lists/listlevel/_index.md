---
title: ListLevel Class
linktitle: ListLevel
articleTitle: ListLevel
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Lists.ListLevel för avancerad listformatering. Förbättra dokumentstrukturen med kraftfulla, anpassningsbara alternativ.
type: docs
weight: 3950
url: /sv/net/aspose.words.lists/listlevel/
---
## ListLevel class

Definierar formatering för en listnivå.

För att lära dig mer, besök[Arbeta med listor](https://docs.aspose.com/words/net/working-with-lists/) dokumentationsartikel.

```csharp
public class ListLevel
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Hämtar eller ställer in justeringen av det faktiska numret på listobjektet. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; set; } | Hämtar eller ställer in det anpassade numeriska formatet för den här listnivån. Till exempel: "a, ç, ĝ, ...". |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Anger teckenformatering som används för listetiketten. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Returnerar bilddata för bildens punktform för den aktuella listnivån. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | Sant om nivån ändrar alla ärvda tal till arabiska, falskt om den bevarar deras talstil. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Hämtar eller ställer in styckeformatet som är länkat till den här listnivån. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Returnerar eller anger talformatet för listnivån. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Returnerar eller anger positionen (i punkter) för numret eller punkten för listnivån. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Returnerar eller anger numerisk stil för denna listnivå. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Ställer in eller returnerar listnivån som måste visas innan den angivna listnivån börjar om numreringen. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Returnerar eller anger startnumret för denna listnivå. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Returnerar eller anger tabbpositionen (i punkter) för listnivån. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Returnerar eller anger positionen (i punkter) för den andra raden med radbrytande text för listnivån. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Returnerar eller anger tecknet som infogas efter numret för listnivån. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Skapar en punktformad bild för den aktuella listnivån. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Tar bort bildpunkten för den aktuella listnivån. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(*ListLevel*) | Jämförs med den angivna ListLevel. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Beräknar hashkod för detta objekt. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(*int, [NumberStyle](../../aspose.words/numberstyle/), string*) | Rapporterar strängrepresentationen av`ListLevel`objekt för det angivna index för listobjektet. Parametrar anger[`NumberStyle`](../../aspose.words/numberstyle/) och ett valfritt format string som används närCustom är specificerad. |

## Anmärkningar

Du skapar inte objekt av den här klassen. Objekt på listnivå skapas automatiskt när en lista skapas. Du får åtkomst`ListLevel` objekt via the [`ListLevelCollection`](../listlevelcollection/) samling.

Använd egenskaperna för`ListLevel` för att ange listformatering för enskilda listnivåer.

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
