---
title: CompositeNode.SelectNodes
linktitle: SelectNodes
articleTitle: SelectNodes
second_title: Aspose.Words för .NET
description: Hämta enkelt noder med CompositeNode SelectNodes-metoden med hjälp av XPath-uttryck för förbättrad datahantering och effektiviserad kodning.
type: docs
weight: 210
url: /sv/net/aspose.words/compositenode/selectnodes/
---
## CompositeNode.SelectNodes method

Väljer en lista med noder som matchar XPath-uttrycket.

```csharp
public NodeList SelectNodes(string xpath)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xpath | String | XPath-uttrycket. |

### Returvärde

En lista över noder som matchar XPath-frågan.

## Anmärkningar

Endast uttryck med elementnamn stöds för närvarande. Expressions som använder attributnamn stöds inte.

## Exempel

Visar hur man använder ett XPath-uttryck för att testa om en nod finns inuti ett fält.

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// NodeList som är resultatet av detta XPath-uttryck kommer att innehålla alla noder vi hittar i ett fält.
// Noderna FieldStart och FieldEnd kan dock finnas med i listan om det finns kapslade fält i sökvägen.
// Hittar för närvarande inga ovanliga fält där FieldCode eller FieldResult sträcker sig över flera stycken.
NodeList resultList =
    doc.SelectNodes("//FältStart/följande-syskon::node()[följande-syskon::FältSlut]");

// Kontrollera om den angivna körningen är en av noderna som finns inuti fältet.
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

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

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
