---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: Aspose.Words para .NET
description: Descubre el método Node NextPreOrder para un recorrido eficiente del árbol. ¡Aprende a recuperar el siguiente nodo usando el algoritmo de preorden de forma eficaz!
type: docs
weight: 130
url: /es/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Obtiene el siguiente nodo según el algoritmo de recorrido del árbol de preorden.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| rootNode | Node | El nodo superior (límite) del recorrido. |

### Valor_devuelto

Siguiente nodo en la preorden. Nulo si se alcanza el*rootNode*.

## Ejemplos

Muestra cómo recorrer el árbol de nodos del documento utilizando el algoritmo de recorrido de preorden y eliminar cualquier forma encontrada con una imagen.

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

### Ver también

* class [Node](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
