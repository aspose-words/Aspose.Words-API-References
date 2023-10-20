---
title: List Class
linktitle: List
articleTitle: List
second_title: Aspose.Words för .NET
description: Aspose.Words.Lists.List klass. Representerar formatering av en lista i C#.
type: docs
weight: 3460
url: /sv/net/aspose.words.lists/list/
---
## List class

Representerar formatering av en lista.

För att lära dig mer, besök[Arbeta med listor](https://docs.aspose.com/words/net/working-with-lists/) dokumentationsartikel.

```csharp
public class List : IComparable<List>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Hämtar ägardokumentet. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | Returnerar`Sann` om den här listan är en definition av en liststil. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | Returnerar`Sann` om den här listan är en referens till en liststil. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | Returnerar`Sann` när listan innehåller 9 nivåer;`falsk` när 1 nivå. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Anger om listan ska startas om vid varje avsnitt. Standardvärdet är`falsk` . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Får den unika identifieraren för listan. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Hämtar samlingen av listnivåer för den här listan. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Hämtar liststilen som den här listan refererar till eller definierar. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(*List*) | Jämför den angivna listan med den aktuella listan. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(*object*) | Jämför det angivna objektet med det aktuella objektet. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(*List*) | Jämför med den angivna listan. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(*object*) | Bestämmer om det angivna objektet har samma värde som det aktuella objektet. |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Beräknar hashkod för detta listobjekt. |
| [HasSameTemplate](../../aspose.words.lists/list/hassametemplate/)(*List*) | Returnerar sant om den aktuella listan och den givna listan skapas från samma mall. |

## Anmärkningar

En lista i ett Microsoft Word-dokument är en uppsättning listformateringsegenskaper. Varje lista kan ha upp till 9 nivåer och formateringsegenskaper, såsom talstil, startvärde, indrag, tabbposition etc definieras separat för varje nivå.

A`List` objektet tillhör alltid[`ListCollection`](../listcollection/) samling.

För att skapa en ny lista, använd Lägg till metoder för[`ListCollection`](../listcollection/) samling.

För att ändra formateringen av en lista, använd[`ListLevel`](../listlevel/) objekt hittade i the[`ListLevels`](./listlevels/) samling.

För att tillämpa eller ta bort listformatering från ett stycke, använd[`ListFormat`](../listformat/).

## Exempel

Visar hur man startar om numrering i en lista genom att kopiera en lista.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda en dokumentbyggares "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slutet kommer att bli ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa dess första listnivå.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Tillämpa vår lista på några stycken.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Vi kan lägga till en kopia av en befintlig lista till dokumentets listsamling
// för att skapa en liknande lista utan att göra ändringar i originalet.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Tillämpa den andra listan på nya stycken.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

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

Visar hur man arbetar med listnivåer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda en dokumentbyggares "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slutet kommer att bli ett objekt i listan.
// Nedan finns två typer av listor som vi kan skapa med hjälp av en dokumentbyggare.
// 1 - En numrerad lista:
// Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje objekt.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Genom att ställa in egenskapen "ListLevelNumber" kan vi öka listnivån
// för att starta en fristående underlista vid det aktuella listobjektet.
// Microsoft Word-listmallen som heter "NumberDefault" använder siffror för att skapa listnivåer för den första listnivån.
 // Djupare listnivåer använder bokstäver och gemener romerska siffror.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - En punktlista:
// Denna lista kommer att tillämpa ett indrag och en punktsymbol ("•") före varje stycke.
// Djupare nivåer i den här listan kommer att använda olika symboler, som "■" och "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Vi kan inaktivera listformatering för att inte formatera några efterföljande stycken som listor genom att avaktivera "List"-flaggan.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Se även

* namnutrymme [Aspose.Words.Lists](../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../)
