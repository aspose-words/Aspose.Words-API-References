---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Node NextPreOrder pour une traversée efficace des arbres. Apprenez à récupérer le nœud suivant grâce à l'algorithme de précommande !
type: docs
weight: 130
url: /fr/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Obtient le nœud suivant selon l'algorithme de parcours de l'arbre de pré-ordre.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| rootNode | Node | Le nœud supérieur (limite) de traversée. |

### Return_Value

Nœud suivant dans l'ordre de précommande. Nul si atteint le*rootNode*.

## Exemples

Montre comment parcourir l'arborescence des nœuds du document à l'aide de l'algorithme de parcours pré-commandé et supprimer toute forme rencontrée avec une image.

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
