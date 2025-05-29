---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: Aspose.Words för .NET
description: Upptäck Node NextPreOrder-metoden för effektiv trädgenomgång. Lär dig hur du effektivt hämtar nästa nod med hjälp av förbeställningsalgoritmen!
type: docs
weight: 130
url: /sv/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| rootNode | Node | Den översta noden (gränsen) för genomfarten. |

### Returvärde

Nästa nod i förbeställningsordningen. Null om nått*rootNode*.

## Exempel

Visar hur man bläddrar i dokumentets nodträd med hjälp av algoritmen för förbeställningsbläddring och tar bort alla påträffade former med en bild.

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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
