---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words para .NET
description: Borre sin esfuerzo todas las respuestas a su comentario con el método RemoveAllReplies, lo que garantiza una discusión sin desorden y una mejor experiencia de usuario.
type: docs
weight: 170
url: /es/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

Elimina todas las respuestas a este comentario.

```csharp
public void RemoveAllReplies()
```

## Observaciones

Todos los nodos constituyentes de las respuestas se eliminarán del documento.

## Ejemplos

Muestra cómo eliminar respuestas a comentarios.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// A continuación se muestran dos formas de eliminar respuestas de un comentario.
// 1 - Utilice el método "RemoveReply" para eliminar las respuestas de un comentario individualmente:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 - Utilice el método "RemoveAllReplies" para eliminar todas las respuestas de un comentario a la vez:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### Ver también

* class [Comment](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
