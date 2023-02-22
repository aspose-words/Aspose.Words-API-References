---
title: CompositeNode.IndexOf
second_title: Referencia de API de Aspose.Words para .NET
description: CompositeNode método. Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios.
type: docs
weight: 130
url: /es/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios.

```csharp
public int IndexOf(Node child)
```

### Observaciones

Devuelve -1 si el nodo no se encuentra en los nodos secundarios.

### Ejemplos

Muestra cómo obtener el índice de un nodo secundario dado de su padre.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// Recuperar el índice del último párrafo en el cuerpo de la primera sección.
Assert.AreEqual(24, body.ChildNodes.IndexOf(body.LastParagraph));
```

### Ver también

* class [Node](../../node/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../compositenode/)
* asamblea [Aspose.Words](../../../)


