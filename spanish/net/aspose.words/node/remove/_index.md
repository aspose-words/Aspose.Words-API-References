---
title: Node.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words para .NET
description: Node Remove método. Se elimina del padre en C#.
type: docs
weight: 150
url: /es/net/aspose.words/node/remove/
---
## Node.Remove method

Se elimina del padre.

```csharp
public void Remove()
```

## Ejemplos

Muestra cómo eliminar todas las formas con imágenes de un documento.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

Muestra cómo eliminar todos los nodos secundarios de un tipo específico de un nodo compuesto.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Guarda el siguiente nodo hermano como una variable en caso de que queramos pasar a él después de eliminar este nodo.
    Node nextNode = curNode.NextSibling;

    // El cuerpo de una sección puede contener nodos de párrafo y tabla.
    // Si el nodo es una tabla, elimínelo del padre.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

### Ver también

* class [Node](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
