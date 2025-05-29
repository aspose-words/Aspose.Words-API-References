---
title: ListCollection Class
linktitle: ListCollection
articleTitle: ListCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Lists.ListCollection för effektiv hantering av punktlistor och numrerade listor, vilket förbättrar dokumentformatering och organisation.
type: docs
weight: 3920
url: /sv/net/aspose.words.lists/listcollection/
---
## ListCollection class

Lagrar och hanterar formatering av punktlistor och numrerade listor som används i ett dokument.

För att lära dig mer, besök[Arbeta med listor](https://docs.aspose.com/words/net/working-with-lists/) dokumentationsartikel.

```csharp
public class ListCollection : IEnumerable<List>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | Hämtar antalet numrerade och punktlistor i dokumentet. |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | Hämtar ägardokumentet. |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | Hämtar en lista efter index. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(*[ListTemplate](../listtemplate/)*) | Skapar en ny lista baserad på en fördefinierad mall och lägger till den i samlingen av listor i dokumentet. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(*[Style](../../aspose.words/style/)*) | Skapar en ny lista som refererar till en liststil och lägger till den i samlingen av listor i dokumentet. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(*[List](../list/)*) | Skapar en ny lista genom att kopiera den angivna listan och lägga till den i samlingen av listor i dokumentet. |
| [AddSingleLevelList](../../aspose.words.lists/listcollection/addsinglelevellist/)(*[ListTemplate](../listtemplate/)*) | Skapar en ny lista på en nivå baserad på den fördefinierade mallen och lägger till den i listsamlingen i dokumentet. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Hämtar enumerator-objektet som räknar upp listor i dokumentet. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(*int*) | Hämtar en lista med hjälp av en listidentifierare. |

## Anmärkningar

En lista i ett Microsoft Word-dokument är en uppsättning listformateringsegenskaper. Listornas formatering lagras i`ListCollection` samling separat från textstycken.

Du skapar inte objekt av den här klassen. Det finns alltid bara ett`ListCollection` -objekt per dokument och det är tillgängligt via[`Lists`](../../aspose.words/documentbase/lists/) egendom.

För att skapa en ny lista baserad på en fördefinierad listmall eller baserat på en liststil, använd[`Add`](./add/) metod.

För att skapa en ny lista med formatering identisk med en befintlig lista, använd[`AddCopy`](./addcopy/) metod.

För att göra ett stycke punktformaterat eller numrerat måste du använda listformatering på ett stycke genom att tilldela en[`List`](../list/)invända mot the [`List`](../listformat/list/) egendom av[`ListFormat`](../listformat/).

För att ta bort listformatering från ett stycke, använd[`RemoveNumbers`](../listformat/removenumbers/) -metoden.

Om du vet lite om WordprocessingML kanske du vet att det definierar separata begrepp för "lista" och "listdefinition". Detta motsvarar exakt hur listformatering lagras i ett Microsoft Word-dokument på låg nivå. Listdefinition är som ett "schema" och lista är som en instans av en listdefinition.

För att förenkla programmeringsmodellen döljer Aspose.Words skillnaden mellan list och list definitioner på ungefär samma sätt som Microsoft Word döljer detta i sitt användargränssnitt. Detta låter dig koncentrera dig mer på hur du vill att ditt dokument ska se ut, snarare än att bygga lågnivåobjekt för att uppfylla kraven i Microsoft Word-filformatet.

Det är inte möjligt att ta bort listor när de väl har skapats i den aktuella versionen av Aspose.Words. . Detta liknar Microsoft Word där användaren inte har explicit kontroll över listdefinitioner.

## Exempel

Visar hur man skapar ett dokument med ett exempel på alla listor från ett annat dokument.

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
}
```

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

* class [List](../list/)
* namnutrymme [Aspose.Words.Lists](../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../)
