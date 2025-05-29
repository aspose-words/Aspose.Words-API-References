---
title: Node.CustomNodeId
linktitle: CustomNodeId
articleTitle: CustomNodeId
second_title: Aspose.Words für .NET
description: Entdecken Sie die Node CustomNodeId-Eigenschaft für eine effiziente benutzerdefinierte Knotenidentifizierung. Verbessern Sie Ihr Projekt mit eindeutigen Kennungen für eine bessere Organisation!
type: docs
weight: 10
url: /de/net/aspose.words/node/customnodeid/
---
## Node.CustomNodeId property

Gibt die benutzerdefinierte Knotenkennung an.

```csharp
public int CustomNodeId { get; set; }
```

## Bemerkungen

Der Standardwert ist Null.

Diese Kennung kann beliebig gesetzt und verwendet werden. Beispielsweise als Schlüssel zum Abrufen externer Daten.

Wichtiger Hinweis: Der angegebene Wert wird nicht in einer Ausgabedatei gespeichert und existiert nur während der Lebensdauer des Knotens.

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
// Beachten Sie, dass die „CustomNodeId“ nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Durchlaufen Sie die Sammlung der unmittelbar untergeordneten Elemente des Absatzes.
// und drucke alle Läufe oder Formen aus, die wir darin finden.
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

* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
