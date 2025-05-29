---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words para .NET
description: Gestiona fácilmente los autores de comentarios con la propiedad Autor del comentario. Devuelve o establece fácilmente los nombres de los autores para mejorar la interacción del usuario y la claridad del contenido.
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

* class [Comment](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
