---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words para .NET
description: Explora el método GetEnumerator de CompositeNode para iterar sin problemas sobre nodos secundarios. ¡Mejora tu eficiencia de codificación con esta potente función!
type: docs
weight: 120
url: /es/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

Proporciona soporte para cada iteración de estilo sobre los nodos secundarios de este nodo.

```csharp
public IEnumerator<Node> GetEnumerator()
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

* class [Node](../../node/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
