---
title: Comment.Ancestor
second_title: Referencia de API de Aspose.Words para .NET
description: Comment propiedad. Devuelve el padreComment objeto. Devolucionesnulo para comentarios de nivel superior.
type: docs
weight: 20
url: /es/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Devuelve el padre[`Comment`](../) objeto. Devoluciones`nulo` para comentarios de nivel superior.

```csharp
public Comment Ancestor { get; }
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

* class [Comment](../)
* espacio de nombres [Aspose.Words](../../comment/)
* asamblea [Aspose.Words](../../../)


