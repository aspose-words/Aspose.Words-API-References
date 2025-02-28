---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: Aspose.Words for .NET
description: Discover the Node NextPreOrder method for efficient tree traversal. Learn how to retrieve the next node using the preorder algorithm effectively!
type: docs
weight: 130
url: /net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Gets next node according to the pre-order tree traversal algorithm.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | Node | The top node (limit) of traversal. |

### Return Value

Next node in pre-order order. Null if reached the *rootNode*.

## Examples

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```csharp
Document doc = new Document(MyDir + "Images.docx");

Assert.AreEqual(9, 
    doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage));

Node curNode = doc;
while (curNode != null)
{
    Node nextNode = curNode.NextPreOrder(doc);

    if (curNode.PreviousPreOrder(doc) != null && nextNode != null)
        Assert.AreEqual(curNode, nextNode.PreviousPreOrder(doc));

    if (curNode.NodeType == NodeType.Shape && ((Shape)curNode).HasImage)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0,
    doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage));
```

### See Also

* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
