---
title: Comment.Ancestor
second_title: Aspose.Words per .NET API Reference
description: Comment proprietà. Restituisce il genitoreComment oggetto. ritornanullo per commenti di primo livello.
type: docs
weight: 20
url: /it/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Restituisce il genitore[`Comment`](../) oggetto. ritorna`nullo` per commenti di primo livello.

```csharp
public Comment Ancestor { get; }
```

### Esempi

Mostra come stampare tutti i commenti di un documento e le relative risposte.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Se un commento non ha un antenato, è un commento di "livello superiore" invece di un commento di tipo risposta.
// Stampa tutti i commenti di livello superiore insieme alle eventuali risposte.
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

### Guarda anche

* class [Comment](../)
* spazio dei nomi [Aspose.Words](../../comment/)
* assemblea [Aspose.Words](../../../)


