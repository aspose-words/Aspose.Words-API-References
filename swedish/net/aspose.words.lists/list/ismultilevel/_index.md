---
title: List.IsMultiLevel
second_title: Aspose.Words för .NET API Referens
description: List fast egendom. ReturnerarSann när listan innehåller 9 nivåerfalsk när 1 nivå.
type: docs
weight: 40
url: /sv/net/aspose.words.lists/list/ismultilevel/
---
## List.IsMultiLevel property

Returnerar`Sann` när listan innehåller 9 nivåer;`falsk` när 1 nivå.

```csharp
public bool IsMultiLevel { get; }
```

### Anmärkningar

Listorna som du skapar med Aspose.Words är alltid flernivålistor och innehåller 9 nivåer.

Microsoft Word 2003 och senare skapar alltid listor med flera nivåer med 9 nivåer. Men i vissa dokument, skapade med tidigare versioner av Microsoft Word, kan du stöta på listor som bara har en nivå.

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

* class [List](../)
* namnutrymme [Aspose.Words.Lists](../../list/)
* hopsättning [Aspose.Words](../../../)


