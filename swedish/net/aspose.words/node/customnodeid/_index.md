---
title: Node.CustomNodeId
linktitle: CustomNodeId
articleTitle: CustomNodeId
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Node CustomNodeId för effektiv identifiering av anpassade noder. Förbättra ditt projekt med unika identifierare för bättre organisation!
type: docs
weight: 10
url: /sv/net/aspose.words/node/customnodeid/
---
## Node.CustomNodeId property

Anger anpassad nodidentifierare.

```csharp
public int CustomNodeId { get; set; }
```

## Anmärkningar

Standardvärdet är noll.

Denna identifierare kan ställas in och användas godtyckligt. Till exempel som en nyckel för att hämta externa data.

Viktigt att notera att det angivna värdet inte sparas i en utdatafil och endast finns under nodens livstid.

## Exempel

Visar hur man navigerar genom en sammansatt nods samling av underordnade noder.

```csharp
Document doc = new Document();

// Lägg till två körningar och en form som underordnade noder i det första stycket i detta dokument.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Observera att 'CustomNodeId' inte sparas i en utdatafil och endast finns under nodens livstid.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterera genom styckets samling av omedelbara underordnade,
// och skriv ut alla körningar eller former som vi hittar inuti.
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

### Se även

* class [Node](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
