---
title: Node.PreviousPreOrder
linktitle: PreviousPreOrder
articleTitle: PreviousPreOrder
second_title: Aspose.Words per .NET
description: Node PreviousPreOrder metodo. Ottiene il nodo precedente in base allalgoritmo di attraversamento dellalbero di preordine in C#.
type: docs
weight: 140
url: /it/net/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method

Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine.

```csharp
public Node PreviousPreOrder(Node rootNode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| rootNode | Node | Il nodo superiore (limite) di attraversamento. |

### Valore di ritorno

Nodo precedente nell'ordine di preordine. Null se raggiunto il*rootNode*.

## Esempi

Mostra come attraversare l'albero dei nodi del documento utilizzando l'algoritmo di attraversamento del preordine ed eliminare qualsiasi forma incontrata con un'immagine.

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
