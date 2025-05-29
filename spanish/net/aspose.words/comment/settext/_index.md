---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words para .NET
description: Descubra el método SetText, una herramienta fácil de usar que simplifica la adición de comentarios, mejora su flujo de trabajo y aumenta la productividad sin esfuerzo.
type: docs
weight: 190
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

## Observaciones

Este método permite establecer rápidamente el texto de un comentario a partir de una cadena. La cadena puede contener saltos de párrafo, lo que creará los párrafos de texto correspondientes en el comentario. Si desea insertar elementos más complejos en el comentario, como marcadores o tablas, o aplicar formato enriquecido, debe usar las clases de nodo adecuadas para crear el texto del comentario.

## Ejemplos

Muestra cómo agregar un comentario a un documento y luego responderlo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Coloque el comentario en un nodo en el cuerpo del documento.
// Este comentario se mostrará en la ubicación de su párrafo,
// fuera del margen derecho de la página, y con una línea punteada que lo conecta a su párrafo.
builder.CurrentParagraph.AppendChild(comment);

// Agregue una respuesta, que aparecerá debajo del comentario principal.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Tanto los comentarios como las respuestas son nodos de comentarios.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

Los comentarios que no responden a otros comentarios son de "nivel superior". No tienen comentarios antecesores.
Assert.Null(comment.Ancestor);

// Las respuestas tienen un comentario de nivel superior anterior.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Ver también

* class [Comment](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
