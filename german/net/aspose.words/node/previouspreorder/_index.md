---
title: Node.PreviousPreOrder
linktitle: PreviousPreOrder
articleTitle: PreviousPreOrder
second_title: Aspose.Words für .NET
description: Node PreviousPreOrder methode. Ruft den vorherigen Knoten gemäß dem PreOrderTreeTraversalAlgorithmus ab in C#.
type: docs
weight: 140
url: /de/net/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method

Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab.

```csharp
public Node PreviousPreOrder(Node rootNode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rootNode | Node | Der oberste Knoten (Grenze) der Durchquerung. |

### Rückgabewert

Vorheriger Knoten in der Vorbestellungsreihenfolge. Null, wenn erreicht*rootNode*.

## Beispiele

Zeigt, wie man den Knotenbaum des Dokuments mit dem Vorbestellungs-Traversalalgorithmus durchläuft und alle gefundenen Formen mit einem Bild löscht.

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
