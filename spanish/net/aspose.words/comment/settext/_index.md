---
title: Comment.SetText
second_title: Referencia de API de Aspose.Words para .NET
description: Comment método. Este es un método conveniente que permite configurar fácilmente el texto del comentario.
type: docs
weight: 180
url: /es/net/aspose.words/comment/settext/
---
## Comment.SetText method

Este es un método conveniente que permite configurar fácilmente el texto del comentario.

```csharp
public void SetText(string text)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| text | String | El nuevo texto del comentario. |

### Observaciones

Este método permite configurar rápidamente el texto de un comentario a partir de una cadena. La cadena puede contener saltos de párrafo, esto creará párrafos de texto en el comentario en consecuencia. Si desea insertar elementos más complejos en el comentario, por ejemplo bookmarks o tablas o aplicar formato enriquecido, entonces necesita usar las clases de nodo apropiadas para construir el texto del comentario.

### Ejemplos

Muestra cómo agregar un comentario a un documento y luego responderlo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Coloca el comentario en un nodo del cuerpo del documento.
// Este comentario aparecerá en la ubicación de su párrafo,
// fuera del margen derecho de la página y con una línea de puntos que la conecta con su párrafo.
builder.CurrentParagraph.AppendChild(comment);

// Agrega una respuesta, que aparecerá debajo del comentario principal.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Los comentarios y las respuestas son ambos nodos de comentarios.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Los comentarios que no responden a otros comentarios son de "nivel superior". No tienen comentarios de antepasados.
Assert.Null(comment.Ancestor);

// Las respuestas tienen un comentario de nivel superior antecesor.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Ver también

* class [Comment](../)
* espacio de nombres [Aspose.Words](../../comment/)
* asamblea [Aspose.Words](../../../)


