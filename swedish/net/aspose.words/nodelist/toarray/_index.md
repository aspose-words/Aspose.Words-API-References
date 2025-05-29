---
title: NodeList.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words för .NET
description: Konvertera enkelt NodeList till en array med ToArray-metoden, vilket förenklar nodmanipulation och förbättrar ditt webbutvecklingsarbetsflöde.
type: docs
weight: 40
url: /sv/net/aspose.words/nodelist/toarray/
---
## NodeList.ToArray method

Kopierar alla noder från samlingen till en ny array med noder.

```csharp
public Node[] ToArray()
```

### Returvärde

En matris med noder.

## Anmärkningar

Du bör inte lägga till/ta bort noder medan du itererar över en samling av noder eftersom det ogiltigförklarar iteratorn och kräver uppdateringar för live-samlingar.

För att kunna lägga till/ta bort noder under iteration, använd den här metoden för att kopiera -noder till en array med fast storlek och sedan iterera över arrayen.

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
* class [NodeList](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
