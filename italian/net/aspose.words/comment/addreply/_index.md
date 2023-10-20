---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words per .NET
description: Comment AddReply metodo. Aggiunge una risposta a questo commento in C#.
type: docs
weight: 120
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
| initial | String | L'autore sigla la risposta. |
| dateTime | DateTime | La data e l'ora della risposta. |
| text | String | Il testo della risposta. |

### Valore di ritorno

Il creato[`Comment`](../) nodo per la risposta.

## Osservazioni

A causa delle limitazioni esistenti di MS Office, nel documento è consentito solo 1 livello di risposte. Un'eccezione di tipoInvalidOperationException verrà generato se questo metodo viene chiamato sul commento di risposta esistente.

## Esempi

Mostra come aggiungere un commento a un documento e quindi rispondere.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Posiziona il commento in un nodo nel corpo del documento.
// Questo commento verrà visualizzato nella posizione del suo paragrafo,
// fuori dal margine destro della pagina e con una linea tratteggiata che lo collega al paragrafo.
builder.CurrentParagraph.AppendChild(comment);

// Aggiunge una risposta, che verrà visualizzata sotto il commento principale.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Commenti e risposte sono entrambi nodi Commento.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// I commenti che non rispondono ad altri commenti sono di "livello superiore". Non hanno commenti sugli antenati.
Assert.Null(comment.Ancestor);

// Le risposte hanno un commento di livello superiore antenato.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Guarda anche

* class [Comment](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
