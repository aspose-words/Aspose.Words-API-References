---
title: List.Style
second_title: Aspose.Words för .NET API Referens
description: List fast egendom. Hämtar liststilen som den här listan refererar till eller definierar.
type: docs
weight: 80
url: /sv/net/aspose.words.lists/list/style/
---
## List.Style property

Hämtar liststilen som den här listan refererar till eller definierar.

```csharp
public Style Style { get; }
```

### Anmärkningar

Om denna lista inte är associerad med en liststil kommer egenskapen att returnera null.

En lista kan i detta fall vara en referens till en liststil[`IsListStyleReference`](../isliststylereference/) kommer att vara sant.

En lista kan vara en definition av en liststil, i det här fallet[`IsListStyleDefinition`](../isliststyledefinition/) kommer att vara sant. En sådan lista kan inte tillämpas på stycken i dokumentet direkt.

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

* class [Style](../../../aspose.words/style/)
* class [List](../)
* namnutrymme [Aspose.Words.Lists](../../list/)
* hopsättning [Aspose.Words](../../../)


