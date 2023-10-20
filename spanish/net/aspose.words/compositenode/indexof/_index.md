---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words para .NET
description: CompositeNode IndexOf método. Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios en C#.
type: docs
weight: 120
url: /es/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios.

```csharp
public int IndexOf(Node child)
```

## Observaciones

Devuelve -1 si el nodo no se encuentra en los nodos secundarios.

## Ejemplos

Muestra cómo obtener el índice de un nodo secundario determinado de su padre.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// Recupera el índice del último párrafo del cuerpo de la primera sección.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### Ver también

* class [Node](../../node/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
