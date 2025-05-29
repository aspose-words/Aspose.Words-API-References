---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words para .NET
description: Mejore sus discusiones con el método Comment AddReply: ¡agregue fácilmente respuestas a los comentarios y mejore la participación en su plataforma!
type: docs
weight: 160
url: /es/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Agrega una respuesta a este comentario.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| author | String | El nombre del autor de la respuesta. |
| initial | String | El autor firma la respuesta. |
| dateTime | DateTime | La fecha y hora de la respuesta. |
| text | String | El texto de respuesta. |

### Valor_devuelto

Lo creado[`Comment`](../) nodo para la respuesta.

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidOperationException | Se lanza si se llama a este método en el comentario de respuesta existente. |

## Observaciones

Debido a las limitaciones existentes de MS Office, solo se permite un nivel de respuestas en el documento.

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
