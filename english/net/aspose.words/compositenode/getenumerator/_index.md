---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
second_title: Aspose.Words for .NET API Reference
description: CompositeNode GetEnumerator method. Provides support for the for each style iteration over the child nodes of this node in C#.
type: docs
weight: 110
url: /net/aspose.words/compositenode/getenumerator/
---
## GetEnumerator method

Provides support for the for each style iteration over the child nodes of this node.

```csharp
public IEnumerator<Node> GetEnumerator()
```

## Examples

Shows how to traverse through a composite node's collection of child nodes.

```csharp
Document doc = new Document();

// Add two runs and one shape as child nodes to the first paragraph of this document.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterate through the paragraph's collection of immediate children,
// and print any runs or shapes that we find within.
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
            break;
    }
```

### See Also

* class [Node](../../node/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../compositenode/)
* assembly [Aspose.Words](../../../)
