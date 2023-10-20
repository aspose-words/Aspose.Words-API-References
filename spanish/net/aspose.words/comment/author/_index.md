---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words para .NET
description: Comment Author propiedad. Devuelve o establece el nombre del autor de un comentario en C#.
type: docs
weight: 30
url: /es/net/aspose.words/comment/author/
---
## Comment.Author property

Devuelve o establece el nombre del autor de un comentario.

```csharp
public string Author { get; set; }
```

## Observaciones

No puede ser`nulo`.

El valor predeterminado es una cadena vacía.

## Ejemplos

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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
