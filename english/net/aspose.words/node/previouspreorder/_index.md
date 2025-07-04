---
title: Node.PreviousPreOrder
linktitle: PreviousPreOrder
articleTitle: PreviousPreOrder
second_title: Aspose.Words for .NET
description: Discover the Node PreviousPreOrder method to efficiently retrieve the prior node using the preorder tree traversal algorithm for optimized data processing.
type: docs
weight: 140
url: /net/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method

Gets the previous node according to the pre-order tree traversal algorithm.

```csharp
public Node PreviousPreOrder(Node rootNode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | Node | The top node (limit) of traversal. |

### Return Value

Previous node in pre-order order. Null if reached the *rootNode*.

## Examples

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```csharp
Document doc = new Document(MyDir + "Images.docx");

Assert.That(doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage), Is.EqualTo(9));

Node curNode = doc;
while (curNode != null)
{
    Node nextNode = curNode.NextPreOrder(doc);

    if (curNode.PreviousPreOrder(doc) != null && nextNode != null)
        Assert.That(nextNode.PreviousPreOrder(doc), Is.EqualTo(curNode));

    if (curNode.NodeType == NodeType.Shape && ((Shape)curNode).HasImage)
        curNode.Remove();

    curNode = nextNode;
}

Assert.That(doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage), Is.EqualTo(0));
```

### See Also

* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
