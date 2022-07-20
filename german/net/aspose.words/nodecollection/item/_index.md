---
title: Item
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft einen Knoten am angegebenen Index ab.
type: docs
weight: 20
url: /de/net/aspose.words/nodecollection/item/
---
## NodeCollection indexer

Ruft einen Knoten am angegebenen Index ab.

```csharp
public Node this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Ein Index in die Sammlung von Knoten. |

### Bemerkungen

Der Index ist nullbasiert.

Negative Indizes sind zulässig und zeigen den Zugriff von der Rückseite der Sammlung an. Zum Beispiel bedeutet -1 das letzte Element, -2 bedeutet das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

### Beispiele

Zeigt, wie die Sammlung untergeordneter Knoten eines zusammengesetzten Knotens durchlaufen wird.

```csharp
Document doc = new Document();

// Fügen Sie dem ersten Absatz dieses Dokuments zwei Läufe und eine Form als untergeordnete Knoten hinzu.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Beachten Sie, dass die 'CustomNodeId' nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Durch die Sammlung der unmittelbaren Kinder des Absatzes iterieren,
// und drucken Sie alle Läufe oder Formen, die wir darin finden.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
    }
```

### Siehe auch

* class [Node](../../node)
* class [NodeCollection](../../nodecollection)
* namensraum [Aspose.Words](../../nodecollection)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->