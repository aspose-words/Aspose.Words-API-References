---
title: Node.NextPreOrder
second_title: Aspose.Words för .NET API Referens
description: Node metod. Hämtar nästa nod enligt algoritmen för förbeställningsträdet.
type: docs
weight: 130
url: /sv/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Hämtar nästa nod enligt algoritmen för förbeställningsträdet.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| rootNode | Node | Den övre noden (gränsen) för traversering. |

### Returvärde

Nästa nod i förbeställning. Null om nått rootNode.

### Exempel

Visar hur man går igenom dokumentets nodträd med förbeställnings-genomgångsalgoritmen och tar bort alla former som påträffas med en bild.

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

### Se även

* class [Node](../)
* namnutrymme [Aspose.Words](../../node/)
* hopsättning [Aspose.Words](../../../)


