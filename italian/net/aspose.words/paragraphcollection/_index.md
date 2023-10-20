---
title: ParagraphCollection Class
linktitle: ParagraphCollection
articleTitle: ParagraphCollection
second_title: Aspose.Words per .NET
description: Aspose.Words.ParagraphCollection classe. Fornisce laccesso digitato a una raccolta diParagraph nodi in C#.
type: docs
weight: 4410
url: /it/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

Fornisce l'accesso digitato a una raccolta di[`Paragraph`](../paragraph/) nodi.

Per saperne di più, visita il[Lavorare con i paragrafi](https://docs.aspose.com/words/net/working-with-paragraphs/) articolo di documentazione.

```csharp
public class ParagraphCollection : NodeCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ottiene il numero di nodi nella raccolta. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | Recupera a[`Paragraph`](../paragraph/) all'indice indicato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Aggiunge un nodo alla fine della raccolta. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Rimuove tutti i nodi da questa raccolta e dal documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Determina se un nodo è nella raccolta. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fornisce una semplice iterazione di stile "foreach" sulla raccolta di nodi. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Restituisce l'indice in base zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Inserisce un nodo nella raccolta in corrispondenza dell'indice specificato. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | Copia tutti i paragrafi dalla raccolta in un nuovo array di paragrafi. (2 methods) |

## Esempi

Mostra come verificare se un paragrafo è una revisione di spostamento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Questo documento contiene revisioni "Sposta", che appaiono quando evidenziamo il testo con il cursore,
// quindi trascinalo per spostarlo in un'altra posizione
// durante il monitoraggio delle revisioni in Microsoft Word tramite "Revisione" -> "Tenere traccia delle modifiche".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Le revisioni di spostamento sono costituite da coppie di revisioni "Sposta da" e "Sposta in".
// Queste revisioni sono potenziali modifiche al documento che possiamo accettare o rifiutare.
// Prima di accettare/rifiutare una revisione di spostamento, il file document
// deve tenere traccia sia della destinazione di partenza che di quella di arrivo del testo.
// Il secondo e il quarto paragrafo definiscono una di queste revisioni e quindi entrambi hanno gli stessi contenuti.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// La revisione "Sposta da" è il paragrafo da cui abbiamo trascinato il testo.
// Se accettiamo la revisione, questo paragrafo scomparirà,
// e l'altro rimarrà e non sarà più una revisione.
Assert.True(paragraphs[1].IsMoveFromRevision);

// La revisione "Sposta in" è il paragrafo in cui abbiamo trascinato il testo.
// Se rifiutiamo la revisione, questo paragrafo invece scomparirà, e l'altro rimarrà.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Guarda anche

* class [NodeCollection](../nodecollection/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
