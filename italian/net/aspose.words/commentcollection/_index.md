---
title: Class CommentCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.CommentCollection classe. Fornisce laccesso digitato a una raccolta diComment nodi.
type: docs
weight: 240
url: /it/net/aspose.words/commentcollection/
---
## CommentCollection class

Fornisce l'accesso digitato a una raccolta di[`Comment`](../comment/) nodi.

Per saperne di più, visita il[Lavorare con i commenti](https://docs.aspose.com/words/net/working-with-comments/) articolo di documentazione.

```csharp
public class CommentCollection : NodeCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ottiene il numero di nodi nella raccolta. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Recupera a[`Comment`](../comment/) all'indice indicato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Aggiunge un nodo alla fine della raccolta. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Rimuove tutti i nodi da questa raccolta e dal documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Determina se un nodo è nella raccolta. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fornisce una semplice iterazione di stile "foreach" sulla raccolta di nodi. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Restituisce l'indice in base zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Inserisce un nodo nella raccolta in corrispondenza dell'indice specificato. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copia tutti i nodi dalla raccolta in un nuovo array di nodi. |

### Esempi

Mostra come contrassegnare un commento come "fatto".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // Inserisci un commento per segnalare un errore.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // I commenti hanno un flag "Fatto", che è impostato su "false" per impostazione predefinita.
// Se un commento suggerisce di apportare una modifica all'interno del documento,
// possiamo applicare la modifica e successivamente impostare anche il flag "Fatto" per indicare la correzione.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// I commenti "finiti" si differenzieranno
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


