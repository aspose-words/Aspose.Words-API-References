---
title: NodeList.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words für .NET
description: Mit der GetEnumerator-Methode iterieren Sie mühelos durch NodeList. Profitieren Sie von einfachem und effizientem Zugriff auf Ihre Knotensammlung in C#.
type: docs
weight: 30
url: /de/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

Bietet eine einfache Iteration im „foreach“-Stil über die Knotensammlung.

```csharp
public IEnumerator<Node> GetEnumerator()
```

### Rückgabewert

Ein IEnumerator.

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
* class [NodeList](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
