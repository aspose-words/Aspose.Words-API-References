---
title: ListCollection.AddCopy
second_title: Aspose.Words för .NET API Referens
description: ListCollection metod. Skapar en ny lista genom att kopiera den angivna listan och lägga till den i samlingen av listor i dokumentet.
type: docs
weight: 50
url: /sv/net/aspose.words.lists/listcollection/addcopy/
---
## ListCollection.AddCopy method

Skapar en ny lista genom att kopiera den angivna listan och lägga till den i samlingen av listor i dokumentet.

```csharp
public List AddCopy(List srcList)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcList | List | Källlistan att kopiera från. |

### Returvärde

Den nyskapade listan.

### Anmärkningar

Källlistan kan vara från vilket dokument som helst. Om källlistan tillhör ett annat dokument, skapas en kopia av listan och läggs till det aktuella dokumentet.

Om källlistan är en referens till eller en definition av en liststil, är den nyskapade listan inte relaterad till den ursprungliga liststilen.

### Exempel

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

### Se även

* class [List](../../list/)
* class [ListCollection](../)
* namnutrymme [Aspose.Words.Lists](../../listcollection/)
* hopsättning [Aspose.Words](../../../)


