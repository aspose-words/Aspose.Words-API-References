---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: Aspose.Words pour .NET
description: Node NextPreOrder méthode. Obtient le nœud suivant selon lalgorithme de traversée de larbre de précommande en C#.
type: docs
weight: 130
url: /fr/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-commande.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| rootNode | Node | Le nœud supérieur (limite) du parcours. |

### Return_Value

Nœud suivant en précommande. Nul si atteint le*rootNode*.

## Exemples

Montre comment parcourir l'arborescence des nœuds du document à l'aide de l'algorithme de parcours de pré-ordre et supprimer toute forme rencontrée avec une image.

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

### Voir également

* class [Node](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
