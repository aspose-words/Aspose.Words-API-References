---
title: CompositeNode.SelectNodes
second_title: Aspose.Words für .NET-API-Referenz
description: CompositeNode methode. Wählt eine Liste von Knoten aus die dem XPathAusdruck entsprechen.
type: docs
weight: 210
url: /de/net/aspose.words/compositenode/selectnodes/
---
## CompositeNode.SelectNodes method

Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen.

```csharp
public NodeList SelectNodes(string xpath)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xpath | String | Der XPath-Ausdruck. |

### Rückgabewert

Eine Liste von Knoten, die der XPath-Abfrage entsprechen.

### Bemerkungen

Derzeit werden nur Ausdrücke mit Elementnamen unterstützt. Expressions , die Attributnamen verwenden, werden nicht unterstützt.

### Beispiele

Zeigt, wie Sie mit einem XPath-Ausdruck testen, ob sich ein Knoten in einem Feld befindet.

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// Die aus diesem XPath-Ausdruck resultierende NodeList enthält alle Knoten, die wir in einem Feld finden.
// FieldStart- und FieldEnd-Knoten können jedoch in der Liste enthalten sein, wenn der Pfad verschachtelte Felder enthält.
// Findet derzeit keine seltenen Felder, in denen sich FieldCode oder FieldResult über mehrere Absätze erstreckt.
NodeList resultList =
    doc.SelectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");

// Prüfen, ob der angegebene Lauf einer der Knoten ist, die sich innerhalb des Feldes befinden.
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

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

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../compositenode/)
* Montage [Aspose.Words](../../../)


