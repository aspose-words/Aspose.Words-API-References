---
title: List Class
linktitle: List
articleTitle: List
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Lists.List för kraftfull listformatering. Förbättra dina dokument med sömlös organisation och professionell presentation.
type: docs
weight: 3910
url: /sv/net/aspose.words.lists/list/
---
## List class

Representerar formateringen av en lista.

För att lära dig mer, besök[Arbeta med listor](https://docs.aspose.com/words/net/working-with-lists/) dokumentationsartikel.

```csharp
public class List : IComparable<List>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Hämtar ägardokumentet. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | Returer`sann` om den här listan är en definition av en liststil. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | Returer`sann` om den här listan är en referens till en liststil. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | Returer`sann` när listan innehåller 9 nivåer;`falsk` när 1 nivå. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Anger om listan ska startas om vid varje avsnitt. Standardvärdet är`falsk` . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Hämtar listans unika identifierare. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Hämtar samlingen av listnivåer för den här listan. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Hämtar liststilen som listan refererar till eller definierar. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(*List*) | Jämför den angivna listan med den aktuella listan. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(*object*) | Jämför det angivna objektet med det aktuella objektet. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(*List*) | Jämförs med den angivna listan. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Beräknar hashkod för detta listobjekt. |
| [HasSameTemplate](../../aspose.words.lists/list/hassametemplate/)(*List*) | Returnerar sant om den aktuella listan och den givna listan skapas från samma mall. |

## Anmärkningar

En lista i ett Microsoft Word-dokument är en uppsättning listformateringsegenskaper. Varje lista kan ha upp till 9 nivåer och formateringsegenskaper, såsom numerisk stil, startvärde, indrag, tabbposition etc. definieras separat för varje nivå.

En`List` föremålet tillhör alltid[`ListCollection`](../listcollection/) samling.

För att skapa en ny lista, använd Add-metoderna i[`ListCollection`](../listcollection/) samling.

För att ändra formateringen av en lista, använd[`ListLevel`](../listlevel/) föremål hittades i [`ListLevels`](./listlevels/) samling.

För att tillämpa eller ta bort listformatering från ett stycke, använd[`ListFormat`](../listformat/).

## Exempel

Visar hur man startar om numreringen i en lista genom att kopiera en lista.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa dess första listnivå.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Tillämpa vår lista på vissa stycken.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Vi kan lägga till en kopia av en befintlig lista i dokumentets listsamling
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

Visar hur man arbetar med listnivåer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Nedan följer två typer av listor som vi kan skapa med hjälp av en dokumentbyggare.
// 1 - En numrerad lista:
// Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje element.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Genom att ställa in egenskapen "ListLevelNumber" kan vi öka listnivån
// för att börja en fristående underlista vid det aktuella listobjektet.
// Listmallen i Microsoft Word som heter "NumberDefault" använder siffror för att skapa listnivåer för den första listnivån.
 // Djupare listnivåer använder bokstäver och gemener romerska siffror.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - En punktlista:
// Den här listan kommer att lägga till ett indrag och en punktsymbol ("•") före varje stycke.
// Djupare nivåer i den här listan kommer att använda andra symboler, såsom "■" och "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Vi kan inaktivera listformatering för att inte formatera några efterföljande stycken som listor genom att avaktivera flaggan "Lista".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Se även

* namnutrymme [Aspose.Words.Lists](../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../)
