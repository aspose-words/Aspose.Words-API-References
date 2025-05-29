---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
articleTitle: SelectSingleNode
second_title: Aspose.Words för .NET
description: Upptäck hur CompositeNodes SelectSingleNode-metod effektivt hämtar den första noden som matchar ditt XPath-uttryck för effektiv datahantering.
type: docs
weight: 220
url: /sv/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

Väljer den första[`Node`](../../node/) som matchar XPath-uttrycket.

```csharp
public Node SelectSingleNode(string xpath)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xpath | String | XPath-uttrycket. |

### Returvärde

Den första[`Node`](../../node/) som matchar XPath-frågan eller`null` om ingen matchande nod hittas.

## Anmärkningar

Endast uttryck med elementnamn stöds för närvarande. Expressions som använder attributnamn stöds inte.

## Exempel

Visar hur man väljer vissa noder med hjälp av ett XPath-uttryck.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Detta uttryck extraherar alla styckenoder,
// som är ättlingar till valfri tabellnod i dokumentet.
NodeList nodeList = doc.SelectNodes("//Tabell//Stycke");

// Iterera genom listan med en uppräknare och skriv ut innehållet i varje stycke i varje cell i tabellen.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Det här uttrycket markerar alla stycken som är direkta underordnade till valfri Body-nod i dokumentet.
nodeList = doc.SelectNodes("//Brödtext/Stycke");

// Vi kan behandla listan som en array.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Använd SelectSingleNode för att välja det första resultatet av samma uttryck som ovan.
Node node = doc.SelectSingleNode("//Brödtext/Stycke");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Se även

* class [Node](../../node/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
