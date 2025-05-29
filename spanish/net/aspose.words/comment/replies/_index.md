---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: Aspose.Words para .NET
description: Descubre las respuestas a comentarios. Accede a una colección de objetos de comentario que son respuestas directas a tu comentario, lo que mejora la interacción del usuario.
type: docs
weight: 110
url: /es/net/aspose.words/comment/replies/
---
## Comment.Replies property

Devuelve una colección de[`Comment`](../) objetos que son hijos inmediatos del comentario especificado.

```csharp
public CommentCollection Replies { get; }
```

## Ejemplos

Muestra cómo imprimir todos los comentarios de un documento y sus respuestas.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Si un comentario no tiene antecesor, es un comentario de "nivel superior" a diferencia de un comentario de tipo respuesta.
// Imprime todos los comentarios de nivel superior junto con cualquier respuesta que puedan tener.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

### Ver también

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
