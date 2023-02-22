---
title: CompositeNode.ChildNodes
second_title: Aspose.Words für .NET-API-Referenz
description: CompositeNode eigendom. Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab.
type: docs
weight: 10
url: /de/net/aspose.words/compositenode/childnodes/
---
## CompositeNode.ChildNodes property

Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab.

```csharp
public NodeCollection ChildNodes { get; }
```

### Bemerkungen

Notiz,`ChildNodes` ist gleichbedeutend mit anrufen`GetChildNodes(NodeType.Any, false)` und erstellt und gibt bei jedem Zugriff eine neue Sammlung zurück.

Wenn keine untergeordneten Knoten vorhanden sind, gibt diese Eigenschaft eine leere Sammlung zurück.

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

* class [NodeCollection](../../nodecollection/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../compositenode/)
* Montage [Aspose.Words](../../../)


