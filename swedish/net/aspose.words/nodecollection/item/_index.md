---
title: NodeCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till vilken nod som helst med NodeCollection Item-egenskapen. Hämta snabbt noder via index för sömlös datahantering och förbättrad prestanda.
type: docs
weight: 20
url: /sv/net/aspose.words/nodecollection/item/
---
## NodeCollection indexer

Hämtar en nod vid det angivna indexet.

```csharp
public Node this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Ett index till samlingen av noder. |

## Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst före sista och så vidare.

Om index är större än eller lika med antalet objekt i listan returnerar detta en nullreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan returnerar detta en null-referens.

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

* class [Node](../../node/)
* class [NodeCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
