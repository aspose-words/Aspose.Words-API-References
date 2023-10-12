---
title: Class ListFormat
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Lists.ListFormat klass. Tillåter att styra vilken listformatering som tillämpas på ett stycke.
type: docs
weight: 3480
url: /sv/net/aspose.words.lists/listformat/
---
## ListFormat class

Tillåter att styra vilken listformatering som tillämpas på ett stycke.

För att lära dig mer, besök[Arbeta med listor](https://docs.aspose.com/words/net/working-with-lists/) dokumentationsartikel.

```csharp
public class ListFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Sant när stycket har en punkt- eller numrerad formatering. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Hämtar eller ställer in listan som detta stycke är medlem i. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Returnerar formateringen på listnivå plus eventuella formateringsöverskridanden som tillämpas på det aktuella stycket. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Hämtar eller ställer in listnivånumret (0 till 8) för stycket. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Startar en ny standard punktlista och tillämpar den på stycket. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Startar en ny standardnumrerad lista och tillämpar den på stycket. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Ökar listnivån för det aktuella stycket med en nivå. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Minskar listnivån för det aktuella stycket med en nivå. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Tar bort siffror eller punkter från det aktuella stycket och ställer in listnivån till noll. |

### Anmärkningar

Ett stycke i ett Microsoft Word-dokument kan punkteras eller numreras. När ett stycke är punkterat eller numrerat, sägs det att listformatering tillämpas på stycket.

Du skapar inte objekt av`ListFormat` klass direkt. Du kommer åt`ListFormat` som en egenskap för ett annat objekt som kan ha listformatering kopplad till sig. För tillfället är objekten som can har listformatering:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) och[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` av en[`Paragraph`](../../aspose.words/paragraph/) anger vilken listformatering och listnivå som tillämpas på det specifika stycket.

`ListFormat` av en[`Style`](../../aspose.words/style/) (tillämplig endast för styckestilar) gör det möjligt att ange vilken listformatering och listnivå som tillämpas på alla stycken i den specifika stilen.

`ListFormat` av en[`DocumentBuilder`](../../aspose.words/documentbuilder/) ger tillgång till listformateringen vid den aktuella markörpositionen inuti[`DocumentBuilder`](../../aspose.words/documentbuilder/).

Själva listformateringen lagras i en[`List`](../list/) objekt som lagras separat från styckena. Listobjekten lagras i en[`ListCollection`](../listcollection/) samling. Det finns en single [`ListCollection`](../listcollection/) insamling pr[`Document`](../../aspose.words/document/).

Styckena hör inte fysiskt till en lista. Styckena just refererar till ett visst listobjekt via[`List`](./list/) property och en viss nivå i listan via[`ListLevelNumber`](./listlevelnumber/) property. Genom att ställa in dessa två egenskaper styr du vilka punkter och numrering som ska tillämpas på ett stycke.

### Exempel

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


