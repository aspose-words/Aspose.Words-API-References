---
title: CommentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente a commenti specifici con la proprietà CommentCollection Item. Recupera i commenti per indice per una gestione semplificata dei contenuti.
type: docs
weight: 10
url: /it/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Recupera un[`Comment`](../../comment/) all'indice dato.

```csharp
public Comment this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice della collezione. |

## Osservazioni

L'indice è basato sullo zero.

Sono consentiti indici negativi che indicano l'accesso dalla parte posteriore della raccolta. Ad esempio -1 indica l'ultimo elemento, -2 indica il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nell'elenco, viene restituito un riferimento null.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, viene restituito un riferimento null.

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

* class [Comment](../../comment/)
* class [CommentCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
