---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: Aspose.Words per .NET
description: Recupera l'oggetto Comment padre con la nostra proprietà Ancestor. Perfetto per navigare tra i thread di commenti e migliorare il coinvolgimento degli utenti.
type: docs
weight: 20
url: /it/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

Restituisce il genitore[`Comment`](../)oggetto. Restituisce`null` per commenti di primo livello.

```csharp
public Comment Ancestor { get; }
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

* class [Comment](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
