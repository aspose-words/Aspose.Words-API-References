---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words per .NET
description: Comment Author proprietà. Restituisce o imposta il nome dellautore per un commento in C#.
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

Non può essere`nullo`.

L'impostazione predefinita è una stringa vuota.

## Esempi

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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
