---
title: NodeCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: NodeCollection Item eigendom. Ruft einen Knoten am angegebenen Index ab in C#.
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
| index | Ein Index für die Sammlung von Knoten. |

## Bemerkungen

Der Index ist nullbasiert.

Negative Indizes sind zulässig und zeigen den Zugriff von der Rückseite der Sammlung an. Beispielsweise bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, wird ein Nullverweis zurückgegeben.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, wird ein Nullverweis zurückgegeben.

## Beispiele

Zeigt, wie die Sammlung untergeordneter Knoten eines zusammengesetzten Knotens durchlaufen wird.

```csharp
Document doc = new Document();

// Fügen Sie dem ersten Absatz dieses Dokuments zwei Läufe und eine Form als untergeordnete Knoten hinzu.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Beachten Sie, dass die „CustomNodeId“ nicht in einer Ausgabedatei gespeichert wird und nur während der Knotenlebensdauer vorhanden ist.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Durch die Sammlung der unmittelbar untergeordneten Elemente des Absatzes iterieren,
// und alle Läufe oder Formen drucken, die wir darin finden.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

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
            break;
    }
```

### Siehe auch

* class [Node](../../node/)
* class [NodeCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
