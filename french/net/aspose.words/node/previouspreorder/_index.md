---
title: Node.PreviousPreOrder
second_title: Référence de l'API Aspose.Words pour .NET
description: Node méthode. Obtient le nœud précédent selon lalgorithme de parcours de larbre de préordre.
type: docs
weight: 140
url: /fr/net/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method

Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre.

```csharp
public Node PreviousPreOrder(Node rootNode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| rootNode | Node | Le nœud supérieur (limite) de traversée. |

### Return_Value

Noeud précédent dans l'ordre de précommande. Null si atteint le rootNode.

### Exemples

Montre comment parcourir l'arborescence de nœuds du document à l'aide de l'algorithme de parcours de pré-commande et supprimer toute forme rencontrée avec une image.

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
* espace de noms [Aspose.Words](../../node/)
* Assemblée [Aspose.Words](../../../)


