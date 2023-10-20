---
title: CompositeNode.SelectNodes
linktitle: SelectNodes
articleTitle: SelectNodes
second_title: Aspose.Words för .NET
description: CompositeNode SelectNodes metod. Väljer en lista med noder som matchar XPathuttrycket i C#.
type: docs
weight: 190
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

Endast uttryck med elementnamn stöds för tillfället. Expressions som använder attributnamn stöds inte.

## Exempel

Visar hur man använder ett XPath-uttryck för att testa om en nod finns i ett fält.

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// NodeList som resulterar från detta XPath-uttryck kommer att innehålla alla noder vi hittar i ett fält.
// FieldStart- och FieldEnd-noder kan dock finnas på listan om det finns kapslade fält i sökvägen.
// Hittar för närvarande inte sällsynta fält där FieldCode eller FieldResult sträcker sig över flera stycken.
NodeList resultList =
    doc.SelectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");

// Kontrollera om den angivna körningen är en av noderna som finns inne i fältet.
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

Visar hur man väljer vissa noder med hjälp av ett XPath-uttryck.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Detta uttryck extraherar alla styckenoder,
// som är ättlingar till valfri tabellnod i dokumentet.
NodeList nodeList = doc.SelectNodes("//Tabell//Paragraph");

// Iterera genom listan med en uppräkning och skriv ut innehållet i varje stycke i varje cell i tabellen.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Detta uttryck kommer att välja alla stycken som är direkta underordnade av någon Kroppsnod i dokumentet.
nodeList = doc.SelectNodes("//Body/Paragraph");

// Vi kan behandla listan som en array.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Använd SelectSingleNode för att välja det första resultatet av samma uttryck som ovan.
Node node = doc.SelectSingleNode("//Body/Paragraph");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Se även

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
