---
title: ListCollection.Add
second_title: Aspose.Words för .NET API Referens
description: ListCollection metod. Skapar en ny lista baserad på en fördefinierad mall och lägger till den i samlingen av listor i dokumentet.
type: docs
weight: 40
url: /sv/net/aspose.words.lists/listcollection/add/
---
## Add(ListTemplate) {#add}

Skapar en ny lista baserad på en fördefinierad mall och lägger till den i samlingen av listor i dokumentet.

```csharp
public List Add(ListTemplate listTemplate)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| listTemplate | ListTemplate | Mallen för listan. |

### Returvärde

Den nyskapade listan.

### Anmärkningar

Aspose.Words listmallar motsvarar de 21 listmallarna available i dialogrutan Bullets and Numbering i Microsoft Word 2003.

Alla listor som skapas med denna metod har 9 listnivåer.

### Exempel

Visar hur man skapar en lista genom att tillämpa ett nytt listformat på en samling stycken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));

List list = doc.Lists.Add(ListTemplate.NumberUppercaseLetterDot);

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = list;
    paragraph.ListFormat.ListLevelNumber = 1;
}

Assert.AreEqual(3, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));
```

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

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* namnutrymme [Aspose.Words.Lists](../../listcollection/)
* hopsättning [Aspose.Words](../../../)

---

## Add(Style) {#add_1}

Skapar en ny lista som refererar till en liststil och lägger till den i samlingen av listor i dokumentet.

```csharp
public List Add(Style listStyle)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| listStyle | Style | Liststilen. |

### Returvärde

Den nyskapade listan.

### Anmärkningar

Den nyskapade listan refererar till liststilen. Om du ändrar egenskaperna för list -stilen återspeglas det i listans egenskaper. Vice versa, om du ändrar egenskaperna för listan, återspeglas det i egenskaperna för liststilen.

### Exempel

Visar hur du skapar en liststil och använder den i ett dokument.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa kapslade listor genom att öka indragsnivån. 
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares "ListFormat"-egenskap. 
// Varje stycke som vi lägger till mellan en listas början och slutet kommer att bli ett objekt i listan.
// Vi kan innehålla ett helt List-objekt i en stil.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Ändra utseendet på alla listnivåer i vår lista.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Skapa en annan lista från en lista inom en stil.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Lägg till några listobjekt som vår lista kommer att formatera.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Skapa och tillämpa en annan lista baserat på liststilen.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Se även

* class [List](../../list/)
* class [Style](../../../aspose.words/style/)
* class [ListCollection](../)
* namnutrymme [Aspose.Words.Lists](../../listcollection/)
* hopsättning [Aspose.Words](../../../)


