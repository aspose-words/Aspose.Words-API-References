---
title: CompositeNode.ChildNodes
second_title: Aspose.Words för .NET API Referens
description: CompositeNode fast egendom. Hämtar alla omedelbara underordnade noder för denna nod.
type: docs
weight: 10
url: /sv/net/aspose.words/compositenode/childnodes/
---
## CompositeNode.ChildNodes property

Hämtar alla omedelbara underordnade noder för denna nod.

```csharp
public NodeCollection ChildNodes { get; }
```

### Anmärkningar

Notera,`ChildNodes` motsvarar att ringa`GetChildNodes(NodeType.Any, false)` och skapar och returnerar en ny samling varje gång den öppnas.

Om det inte finns några underordnade noder returnerar den här egenskapen en tom samling.

### Exempel

Visar hur man går igenom en sammansatt nods samling av undernoder.

```csharp
Document doc = new Document();

// Lägg till två körningar och en form som underordnade noder i det första stycket i detta dokument.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Observera att 'CustomNodeId' inte sparas i en utdatafil och endast existerar under nodens livstid.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterera genom styckets samling av närmaste barn,
// och skriv ut alla körningar eller former som vi hittar inom.
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

### Se även

* class [NodeCollection](../../nodecollection/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../compositenode/)
* hopsättning [Aspose.Words](../../../)


