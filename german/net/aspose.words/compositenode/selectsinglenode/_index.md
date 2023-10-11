---
title: CompositeNode.SelectSingleNode
second_title: Aspose.Words für .NET-API-Referenz
description: CompositeNode methode. Wählt den ersten ausNode das entspricht dem XPathAusdruck.
type: docs
weight: 220
url: /de/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

Wählt den ersten aus[`Node`](../../node/) das entspricht dem XPath-Ausdruck.

```csharp
public Node SelectSingleNode(string xpath)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xpath | String | Der XPath-Ausdruck. |

### Rückgabewert

Der erste[`Node`](../../node/) das mit der XPath-Abfrage übereinstimmt oder`Null` wenn kein passender Knoten gefunden wird.

### Bemerkungen

Derzeit werden nur Ausdrücke mit Elementnamen unterstützt. Expressions , die Attributnamen verwenden, werden nicht unterstützt.

### Beispiele

Zeigt, wie bestimmte Knoten mithilfe eines XPath-Ausdrucks ausgewählt werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Dieser Ausdruck extrahiert alle Absatzknoten,
// die Nachkommen eines beliebigen Tabellenknotens im Dokument sind.
NodeList nodeList = doc.SelectNodes("//Tabelle//Absatz");

// Mit einem Enumerator die Liste durchlaufen und den Inhalt jedes Absatzes in jeder Zelle der Tabelle ausgeben.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Dieser Ausdruck wählt alle Absätze aus, die direkte untergeordnete Elemente eines beliebigen Body-Knotens im Dokument sind.
nodeList = doc.SelectNodes("//Körperabschnitt");

// Wir können die Liste als Array behandeln.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Verwenden Sie SelectSingleNode, um das erste Ergebnis desselben Ausdrucks wie oben auszuwählen.
Node node = doc.SelectSingleNode("//Körperabschnitt");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Siehe auch

* class [Node](../../node/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../compositenode/)
* Montage [Aspose.Words](../../../)


