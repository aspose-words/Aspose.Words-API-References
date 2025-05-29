---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words per .NET
description: Scopri il metodo SetText, uno strumento intuitivo che semplifica l'aggiunta di commenti, migliorando il flusso di lavoro e incrementando la produttività senza sforzo.
type: docs
weight: 190
url: /it/net/aspose.words/comment/settext/
---
## Comment.SetText method

Questo è un metodo comodo che consente di impostare facilmente il testo del commento.

```csharp
public void SetText(string text)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| text | String | Il nuovo testo del commento. |

## Osservazioni

Questo metodo permette di impostare rapidamente il testo di un commento da una stringa. La stringa può contenere interruzioni di paragrafo, che creeranno paragrafi di testo nel commento. Se si desidera inserire elementi più complessi nel commento, ad esempio segnalibri o tabelle, o applicare una formattazione avanzata, è necessario utilizzare le classi di nodi appropriate per creare il testo del commento.

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
