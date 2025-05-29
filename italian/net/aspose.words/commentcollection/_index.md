---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.CommentCollection per accedere facilmente ai nodi Commento, migliorando la modifica dei documenti e la collaborazione nei tuoi progetti.
type: docs
weight: 430
url: /it/net/aspose.words/commentcollection/
---
## CommentCollection class

Fornisce accesso tipizzato a una raccolta di[`Comment`](../comment/) nodi.

Per saperne di più, visita il[Lavorare con i commenti](https://docs.aspose.com/words/net/working-with-comments/) articolo di documentazione.

```csharp
public class CommentCollection : NodeCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ottiene il numero di nodi nella raccolta. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Recupera un[`Comment`](../comment/) all'indice dato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Aggiunge un nodo alla fine della raccolta. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Rimuove tutti i nodi da questa raccolta e dal documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Determina se un nodo è nella raccolta. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fornisce una semplice iterazione in stile "foreach" sulla raccolta di nodi. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Inserisce un nodo nella raccolta all'indice specificato. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copia tutti i nodi dalla raccolta in un nuovo array di nodi. |

## Esempi

Mostra come contrassegnare un commento come "fatto".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // Inserisci un commento per segnalare un errore.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // I commenti hanno un flag "Fatto", che per impostazione predefinita è impostato su "false".
// Se un commento suggerisce di apportare una modifica al documento,
// possiamo applicare la modifica e poi impostare il flag "Fatto" per indicare la correzione.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// I commenti "fatti" si differenzieranno
// da quelli che non sono "finiti" con un colore del testo sbiadito.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### Guarda anche

* class [NodeCollection](../nodecollection/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
