---
title: List.IsListStyleReference
linktitle: IsListStyleReference
articleTitle: IsListStyleReference
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IsListStyleReference. Den indikerar om en lista refererar till en specifik stil, vilket förbättrar dokumentets formatering och organisation.
type: docs
weight: 30
url: /sv/net/aspose.words.lists/list/isliststylereference/
---
## List.IsListStyleReference property

Returer`sann` om den här listan är en referens till en liststil.

```csharp
public bool IsListStyleReference { get; }
```

## Anmärkningar

Observera att det inte har någon effekt att ändra egenskaper för en lista som refererar till en liststil. Listformateringen som anges i själva liststilen har alltid företräde.

## Exempel

Visar hur man skapar en liststil och använder den i ett dokument.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
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

// Skapa och tillämpa en annan lista baserat på listformatet.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Se även

* class [List](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
