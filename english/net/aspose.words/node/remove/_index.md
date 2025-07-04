---
title: Node.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Discover the Node Remove method to effortlessly detach nodes from their parent, enhancing your code's efficiency and structure.
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

Assert.That(shapes.OfType<Shape>().Count(s => s.HasImage), Is.EqualTo(9));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.That(shapes.OfType<Shape>().Count(s => s.HasImage), Is.EqualTo(0));
```

Shows how to remove all child nodes of a specific type from a composite node.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.That(doc.GetChildNodes(NodeType.Table, true).Count, Is.EqualTo(2));

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

Assert.That(doc.GetChildNodes(NodeType.Table, true).Count, Is.EqualTo(0));
```

### See Also

* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
