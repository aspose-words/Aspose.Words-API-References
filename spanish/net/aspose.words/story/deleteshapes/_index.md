---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: Aspose.Words para .NET
description: Elimina fácilmente todas las formas del texto de tu historia con el método DeleteShapes. ¡Simplifica tu contenido y mejora la claridad hoy mismo!
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

// Use un DocumentBuilder para insertar una forma. Esta es una forma en línea.
// que tiene un párrafo padre, que es un nodo hijo del cuerpo de la primera sección.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

//Podemos eliminar todas las formas de los párrafos secundarios de este Cuerpo.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ver también

* class [Story](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
