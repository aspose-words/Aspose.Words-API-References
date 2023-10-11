---
title: Comment.SetText
second_title: Aspose.Words per .NET API Reference
description: Comment metodo. Questo è un metodo comodo che consente di impostare facilmente il testo del commento.
type: docs
weight: 180
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

### Osservazioni

Questo metodo consente di impostare rapidamente il testo di un commento da una stringa. La stringa può contenere interruzioni di paragrafo, questo creerà paragrafi di testo nel commento di conseguenza. Se desideri inserire elementi più complessi nel commento, ad esempio segnalibri o tabelle o applicare la formattazione avanzata, devi utilizzare le classi del nodo appropriate per creare il testo del commento.

### Esempi

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
* spazio dei nomi [Aspose.Words](../../comment/)
* assemblea [Aspose.Words](../../../)


