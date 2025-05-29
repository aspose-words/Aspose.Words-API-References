---
title: List.IsMultiLevel
linktitle: IsMultiLevel
articleTitle: IsMultiLevel
second_title: Aspose.Words för .NET
description: Upptäck om din lista stöder flera nivåer! Vårt verktyg visar sant för 9 nivåer och falskt för 1, vilket förbättrar effektiviteten i din datahantering.
type: docs
weight: 40
url: /sv/net/aspose.words.lists/list/ismultilevel/
---
## List.IsMultiLevel property

Returer`sann` när listan innehåller 9 nivåer;`falsk` när 1 nivå.

```csharp
public bool IsMultiLevel { get; }
```

## Anmärkningar

Listorna som du skapar med Aspose.Words är alltid listor med flera nivåer och innehåller 9 nivåer.

Microsoft Word 2003 och senare skapar alltid listor med flera nivåer och 9 nivåer. Men i vissa dokument som skapats med tidigare versioner av Microsoft Word kan du stöta på listor som bara har 1 nivå.

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
