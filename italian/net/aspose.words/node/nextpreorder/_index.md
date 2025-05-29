---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: Aspose.Words per .NET
description: Scopri il metodo Node NextPreOrder per un attraversamento efficiente degli alberi. Impara come recuperare il nodo successivo utilizzando efficacemente l'algoritmo di preordine!
type: docs
weight: 130
url: /it/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| rootNode | Node | Il nodo superiore (limite) dell'attraversamento. |

### Valore di ritorno

Nodo successivo in ordine di preordine. Null se raggiunto*rootNode*.

## Esempi

Mostra come attraversare l'albero dei nodi del documento utilizzando l'algoritmo di attraversamento pre-ordine ed eliminare qualsiasi forma incontrata con un'immagine.

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

### Guarda anche

* class [Node](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
