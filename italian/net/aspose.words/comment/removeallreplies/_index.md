---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words per .NET
description: Cancella senza sforzo tutte le risposte al tuo commento con il metodo RemoveAllReplies, assicurandoti una discussione ordinata e un'esperienza utente migliorata.
type: docs
weight: 170
url: /it/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

Rimuove tutte le risposte a questo commento.

```csharp
public void RemoveAllReplies()
```

## Osservazioni

Tutti i nodi costituenti le risposte verranno eliminati dal documento.

## Esempi

Mostra come rimuovere le risposte ai commenti.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// Di seguito sono riportati due metodi per rimuovere le risposte da un commento.
// 1 - Utilizzare il metodo "RemoveReply" per rimuovere singolarmente le risposte da un commento:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 - Utilizza il metodo "RemoveAllReplies" per rimuovere tutte le risposte da un commento in una sola volta:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### Guarda anche

* class [Comment](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
