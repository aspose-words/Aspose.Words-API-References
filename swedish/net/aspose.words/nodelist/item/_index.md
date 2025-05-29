---
title: NodeList.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till specifika noder med egenskapen NodeList Item. Hämta noder via index för strömlinjeformad datahantering och effektiv kodning.
type: docs
weight: 20
url: /sv/net/aspose.words/nodelist/item/
---
## NodeList indexer

Hämtar en nod vid det angivna indexet.

```csharp
public Node this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Ett index i listan över noder. |

## Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst före sista och så vidare.

Om index är större än eller lika med antalet objekt i listan returnerar detta en nullreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan returnerar detta en null-referens.

## Exempel

Visar hur man använder XPaths för att navigera i en NodeList.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga några noder med en DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

builder.InsertImage(ImageDir + "Logo.jpg");

// Vårt dokument innehåller tre Run-noder.
NodeList nodeList = doc.SelectNodes("//Sikt");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Använd ett dubbelt snedstreck för att markera alla Run-noder
// som är indirekta ättlingar till en tabellnod, vilket skulle vara körningarna inuti de två cellerna vi infogade.
nodeList = doc.SelectNodes("//Table//Sikt");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Enkla snedstreck anger direkta efterkommande relationer,
// vilket vi hoppade över när vi använde dubbla snedstreck.
Assert.AreEqual(doc.SelectNodes(" //Tabell//Körning"),
    doc.SelectNodes("//Tabell/Rad/Cell/Stycke/Körning"));

// Åtkomst till formen som innehåller bilden vi infogade.
nodeList = doc.SelectNodes("//Form");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Se även

* class [Node](../../node/)
* class [NodeList](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
