---
title: NodeList.ToArray
second_title: Aspose.Words für .NET-API-Referenz
description: NodeList methode. Kopiert alle Knoten aus der Sammlung in ein neues Array von Knoten.
type: docs
weight: 40
url: /de/net/aspose.words/nodelist/toarray/
---
## NodeList.ToArray method

Kopiert alle Knoten aus der Sammlung in ein neues Array von Knoten.

```csharp
public Node[] ToArray()
```

### Rückgabewert

Ein Array von Knoten.

### Bemerkungen

Sie sollten keine Knoten hinzufügen/entfernen, während Sie über eine Sammlung von von Knoten iterieren, da dies den Iterator ungültig macht und Aktualisierungen für Live-Sammlungen erfordert.

Um Knoten während der Iteration hinzufügen/entfernen zu können, verwenden Sie diese Methode, um Knoten in ein Array mit fester Größe zu kopieren und dann über das Array zu iterieren.

### Beispiele

Zeigt, wie bestimmte Knoten mithilfe eines XPath-Ausdrucks ausgewählt werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Dieser Ausdruck extrahiert alle Absatzknoten,
// die Nachkommen eines beliebigen Tabellenknotens im Dokument sind.
NodeList nodeList = doc.SelectNodes("//Tabelle//Absatz");

// Die Liste mit einem Enumerator durchlaufen und den Inhalt jedes Absatzes in jeder Zelle der Tabelle ausgeben.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Dieser Ausdruck wählt alle Absätze aus, die direkte Kinder eines beliebigen Body-Knotens im Dokument sind.
nodeList = doc.SelectNodes("//Körperabschnitt");

// Wir können die Liste als Array behandeln.
Assert.AreEqual(4, nodeList.ToArray().Length);

// SelectSingleNode verwenden, um das erste Ergebnis desselben Ausdrucks wie oben auszuwählen.
Node node = doc.SelectSingleNode("//Körperabschnitt");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Siehe auch

* class [Node](../../node/)
* class [NodeList](../)
* namensraum [Aspose.Words](../../nodelist/)
* Montage [Aspose.Words](../../../)


