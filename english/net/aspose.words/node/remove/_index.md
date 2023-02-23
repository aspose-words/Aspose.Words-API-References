---
title: Node.Remove
linktitle: Remove
second_title: Aspose.Words for .NET API Reference
description: Node method. Removes itself from the parent in C#.
type: docs
weight: 150
url: /net/aspose.words/node/remove/
---
## Node.Remove method

Removes itself from the parent.

```csharp
public void Remove()
```

## Examples

Shows how to delete all shapes with images from a document.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

Shows how to remove all child nodes of a specific type from a composite node.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Save the next sibling node as a variable in case we want to move to it after deleting this node.
    Node nextNode = curNode.NextSibling;

    // A section body can contain Paragraph and Table nodes.
    // If the node is a Table, remove it from the parent.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

### See Also

* class [Node](../)
* namespace [Aspose.Words](../../node/)
* assembly [Aspose.Words](../../../)
