---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words per .NET
description: Gestisci gli autori dei commenti in modo semplice con la proprietà Autore del commento. Restituisci o imposta facilmente i nomi degli autori per migliorare il coinvolgimento degli utenti e la chiarezza dei contenuti.
type: docs
weight: 30
url: /it/net/aspose.words/comment/author/
---
## Comment.Author property

Restituisce o imposta il nome dell'autore per un commento.

```csharp
public string Author { get; set; }
```

## Osservazioni

Non può essere`null`.

Il valore predefinito è una stringa vuota.

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
