---
title: Comment.RemoveReply
linktitle: RemoveReply
articleTitle: RemoveReply
second_title: Aspose.Words para .NET
description: Comment RemoveReply método. Elimina la respuesta especificada a este comentario en C#.
type: docs
weight: 140
url: /es/net/aspose.words/comment/removereply/
---
## Comment.RemoveReply method

Elimina la respuesta especificada a este comentario.

```csharp
public void RemoveReply(Comment reply)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| reply | Comment | El nodo de comentarios de la respuesta de eliminación. |

## Observaciones

Todos los nodos constituyentes de la respuesta se eliminarán del documento.

## Ejemplos

Muestra cómo eliminar respuestas a comentarios.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count()); 

// A continuación se muestran dos formas de eliminar respuestas de un comentario.
// 1 - Utiliza el método "RemoveReply" para eliminar las respuestas de un comentario individualmente:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count());

// 2 - Utilice el método "RemoveAllReplies" para eliminar todas las respuestas de un comentario a la vez:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count());
```

### Ver también

* class [Comment](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
