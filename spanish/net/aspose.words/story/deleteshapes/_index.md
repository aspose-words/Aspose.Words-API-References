---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: Aspose.Words para .NET
description: Story DeleteShapes método. Elimina todas las formas del texto de esta historia en C#.
type: docs
weight: 70
url: /es/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

Elimina todas las formas del texto de esta historia.

```csharp
public void DeleteShapes()
```

## Ejemplos

Muestra cómo eliminar todas las formas de un nodo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Usa un DocumentBuilder para insertar una forma. Esta es una forma en línea,
// que tiene un párrafo principal, que es un nodo secundario del cuerpo de la primera sección.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Podemos eliminar todas las formas de los párrafos secundarios de este cuerpo.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ver también

* class [Story](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
