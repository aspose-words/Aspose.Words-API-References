---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words para .NET
description: Node Clone método. Crea un duplicado del nodo en C#.
type: docs
weight: 100
url: /es/net/aspose.words/node/clone/
---
## Node.Clone method

Crea un duplicado del nodo.

```csharp
public Node Clone(bool isCloneChildren)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| isCloneChildren | Boolean | True para clonar recursivamente el subárbol bajo el nodo especificado; false para clonar solo el nodo. |

### Valor_devuelto

El nodo clonado.

## Observaciones

Este método sirve como constructor de copias para nodos. El nodo clonado no tiene padre, pero pertenece al mismo documento que el nodo original.

Este método siempre realiza una copia profunda del nodo. El*isCloneChildren* parámetro especifica si se deben copiar también todos los nodos secundarios.

## Ejemplos

Muestra cómo clonar un nodo compuesto.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// A continuación se muestran dos formas de clonar un nodo compuesto.
// 1: crea un clon de un nodo y también crea un clon de cada uno de sus nodos secundarios.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Crea un clon de un nodo solo sin ningún hijo.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### Ver también

* class [Node](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
