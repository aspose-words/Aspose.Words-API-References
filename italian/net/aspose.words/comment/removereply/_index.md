---
title: Comment.RemoveReply
linktitle: RemoveReply
articleTitle: RemoveReply
second_title: Aspose.Words per .NET
description: Rimuovi facilmente le risposte indesiderate con il metodo "Comment RemoveReply", assicurandoti che le tue discussioni rimangano chiare e pertinenti. Migliora la tua gestione dei commenti oggi stesso!
type: docs
weight: 180
url: /it/net/aspose.words/comment/removereply/
---
## Comment.RemoveReply method

Rimuove la risposta specificata a questo commento.

```csharp
public void RemoveReply(Comment reply)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| reply | Comment | Il nodo commento della risposta di eliminazione. |

## Osservazioni

Tutti i nodi costituenti la risposta verranno eliminati dal documento.

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
