---
title: Comment.Replies
second_title: Referencia de API de Aspose.Words para .NET
description: Comment propiedad. Devuelve una colección deComment objetos que son hijos inmediatos del comentario especificado.
type: docs
weight: 100
url: /es/net/aspose.words/comment/replies/
---
## Comment.Replies property

Devuelve una colección de[`Comment`](../) objetos que son hijos inmediatos del comentario especificado.

```csharp
public CommentCollection Replies { get; }
```

### Ejemplos

Muestra cómo imprimir todos los comentarios de un documento y sus respuestas.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Si un comentario no tiene antepasado, es un comentario de "nivel superior" en lugar de un comentario de tipo respuesta.
// Imprime todos los comentarios de nivel superior junto con las respuestas que puedan tener.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
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
* espacio de nombres [Aspose.Words](../../comment/)
* asamblea [Aspose.Words](../../../)


