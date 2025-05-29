---
title: NodeList.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: Iterera enkelt genom NodeList med GetEnumerator-metoden. Få enkel och effektiv åtkomst till din samling av noder i C#.
type: docs
weight: 30
url: /sv/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

Ger en enkel iteration i "foreach"-stil över samlingen av noder.

```csharp
public IEnumerator<Node> GetEnumerator()
```

### Returvärde

En IEnumerator.

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
