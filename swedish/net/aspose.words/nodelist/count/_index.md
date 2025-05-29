---
title: NodeList.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words för .NET
description: Upptäck egenskapen NodeList Count för att enkelt hämta det totala antalet noder i din lista, vilket förbättrar din webbutvecklings effektivitet.
type: docs
weight: 10
url: /sv/net/aspose.words/nodelist/count/
---
## NodeList.Count property

Hämtar antalet noder i listan.

```csharp
public int Count { get; }
```

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

* class [NodeList](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
