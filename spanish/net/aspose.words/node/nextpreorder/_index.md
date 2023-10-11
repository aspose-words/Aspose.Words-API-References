---
title: Node.NextPreOrder
second_title: Referencia de API de Aspose.Words para .NET
description: Node método. Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados.
type: docs
weight: 130
url: /es/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| rootNode | Node | El nodo superior (límite) de recorrido. |

### Valor_devuelto

Siguiente nodo en orden de reserva. Nulo si se alcanza el*rootNode*.

### Ejemplos

Muestra cómo recorrer el árbol de nodos del documento utilizando el algoritmo transversal de pedido previo y eliminar cualquier forma encontrada con una imagen.

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
* espacio de nombres [Aspose.Words](../../node/)
* asamblea [Aspose.Words](../../../)


