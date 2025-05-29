---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: Aspose.Words für .NET
description: Entdecken Sie die Node-NextPreOrder-Methode für effizientes Durchlaufen von Baumstrukturen. Erfahren Sie, wie Sie den nächsten Knoten mithilfe des Preorder-Algorithmus effektiv abrufen!
type: docs
weight: 130
url: /de/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rootNode | Node | Der oberste Knoten (Grenze) der Durchquerung. |

### Rückgabewert

Nächster Knoten in der Vorbestellungsreihenfolge. Null, wenn der*rootNode*.

## Beispiele

Zeigt, wie der Knotenbaum des Dokuments mithilfe des Pre-Order-Traversal-Algorithmus durchlaufen und alle gefundenen Formen mit einem Bild gelöscht werden.

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

### Siehe auch

* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
