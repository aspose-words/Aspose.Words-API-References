---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
articleTitle: SelectSingleNode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SelectSingleNode-Methode von CompositeNode effizient den ersten Knoten abruft, der Ihrem XPath-Ausdruck entspricht, und so die Datenverarbeitung optimiert.
type: docs
weight: 220
url: /de/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

Wählt den ersten[`Node`](../../node/) das dem XPath-Ausdruck entspricht.

```csharp
public Node SelectSingleNode(string xpath)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xpath | String | Der XPath-Ausdruck. |

### Rückgabewert

Der erste[`Node`](../../node/) die mit der XPath-Abfrage übereinstimmt oder`null` wenn kein passender Knoten gefunden wird.

## Bemerkungen

Derzeit werden nur Ausdrücke mit Elementnamen unterstützt. Ausdrücke , die Attributnamen verwenden, werden nicht unterstützt.

## Beispiele

Zeigt, wie bestimmte Knoten mithilfe eines XPath-Ausdrucks ausgewählt werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Dieser Ausdruck extrahiert alle Absatzknoten,
// die Nachkommen eines beliebigen Tabellenknotens im Dokument sind.
NodeList nodeList = doc.SelectNodes("//Tabelle//Absatz");

// Mit einem Enumerator durch die Liste iterieren und den Inhalt jedes Absatzes in jeder Zelle der Tabelle drucken.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Dieser Ausdruck wählt alle Absätze aus, die direkte untergeordnete Elemente eines beliebigen Body-Knotens im Dokument sind.
nodeList = doc.SelectNodes("//Textkörper/Absatz");

// Wir können die Liste als Array behandeln.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Verwenden Sie SelectSingleNode, um das erste Ergebnis desselben Ausdrucks wie oben auszuwählen.
Node node = doc.SelectSingleNode("//Textkörper/Absatz");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Siehe auch

* class [Node](../../node/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
