---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: Aspose.Words per .NET
description: Scopri le Risposte ai Commenti. Accedi a una raccolta di oggetti Commento che sono risposte dirette al tuo commento specificato, migliorando il coinvolgimento e l'interazione degli utenti.
type: docs
weight: 110
url: /it/net/aspose.words/comment/replies/
---
## Comment.Replies property

Restituisce una raccolta di[`Comment`](../) oggetti che sono figli immediati del commento specificato.

```csharp
public CommentCollection Replies { get; }
```

## Esempi

Mostra come stampare tutti i commenti di un documento e le relative risposte.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Se un commento non ha antenati, si tratta di un commento di "livello superiore" e non di un commento di tipo risposta.
// Stampa tutti i commenti di primo livello insieme alle eventuali risposte.
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

### Guarda anche

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
