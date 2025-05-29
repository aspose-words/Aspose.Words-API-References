---
title: Story.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words para .NET
description: Descubra la propiedad StoryType para identificar y categorizar fácilmente sus historias, mejorando la organización y optimizando su experiencia narrativa.
type: docs
weight: 40
url: /es/net/aspose.words/story/storytype/
---
## Story.StoryType property

Obtiene el tipo de esta historia.

```csharp
public StoryType StoryType { get; }
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

* enum [StoryType](../../storytype/)
* class [Story](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
