---
title: Node.PreviousPreOrder
linktitle: PreviousPreOrder
articleTitle: PreviousPreOrder
second_title: Aspose.Words för .NET
description: Upptäck Node PreviousPreOrder-metoden för att effektivt hämta den tidigare noden med hjälp av förbeställningsträdets traverseringsalgoritm för optimerad databehandling.
type: docs
weight: 140
url: /sv/net/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method

Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning.

```csharp
public Node PreviousPreOrder(Node rootNode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| rootNode | Node | Den översta noden (gränsen) för genomfarten. |

### Returvärde

Föregående nod i förbeställningsordern. Null om nått*rootNode*.

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
