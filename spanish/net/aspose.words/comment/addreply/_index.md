---
title: Comment.AddReply
second_title: Referencia de API de Aspose.Words para .NET
description: Comment método. Agrega una respuesta a este comentario.
type: docs
weight: 150
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
| initial | String | El autor pone sus iniciales en la respuesta. |
| dateTime | DateTime | La fecha y hora de la respuesta. |
| text | String | El texto de respuesta. |

### Valor_devuelto

el creado[`Comment`](../) nodo para la respuesta.

### Observaciones

Debido a las limitaciones existentes de MS Office, solo se permite 1 nivel de respuestas en el documento. Una excepción de tipoInvalidOperationException se generará si se llama a este método en el comentario de respuesta existente.

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


