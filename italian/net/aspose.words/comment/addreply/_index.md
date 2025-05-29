---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words per .NET
description: Arricchisci le tue discussioni con il metodo Comment AddReply: aggiungi facilmente risposte ai commenti e migliora il coinvolgimento sulla tua piattaforma!
type: docs
weight: 160
url: /it/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Aggiunge una risposta a questo commento.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| author | String | Il nome dell'autore della risposta. |
| initial | String | Le iniziali dell'autore per la risposta. |
| dateTime | DateTime | Data e ora della risposta. |
| text | String | Il testo di risposta. |

### Valore di ritorno

Il creato[`Comment`](../) nodo per la risposta.

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidOperationException | Generato se questo metodo viene chiamato sul commento Reply esistente. |

## Osservazioni

A causa delle limitazioni esistenti di MS Office, nel documento è consentito solo 1 livello di risposte.

## Esempi

Mostra come aggiungere un commento a un documento e poi rispondere.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Posiziona il commento in un nodo del corpo del documento.
// Questo commento verrà visualizzato nella posizione del suo paragrafo,
// fuori dal margine destro della pagina e con una linea tratteggiata che lo collega al suo paragrafo.
builder.CurrentParagraph.AppendChild(comment);

// Aggiungi una risposta, che verrà visualizzata sotto il commento padre.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Sia i commenti che le risposte sono nodi Commento.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// I commenti che non rispondono ad altri commenti sono di "livello superiore". Non hanno commenti precedenti.
Assert.Null(comment.Ancestor);

// Le risposte hanno un commento di primo livello antenato.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Guarda anche

* class [Comment](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
