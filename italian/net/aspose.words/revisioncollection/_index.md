---
title: RevisionCollection Class
linktitle: RevisionCollection
articleTitle: RevisionCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.RevisionCollection gestisci in modo efficiente le revisioni dei documenti con una potente raccolta di oggetti Revision per una modifica fluida.
type: docs
weight: 5510
url: /it/net/aspose.words/revisioncollection/
---
## RevisionCollection class

Una raccolta di[`Revision`](../revision/) oggetti che rappresentano revisioni nel documento.

Per saperne di più, visita il[Traccia le modifiche in un documento](https://docs.aspose.com/words/net/track-changes-in-a-document/) articolo di documentazione.

```csharp
public class RevisionCollection : IEnumerable<Revision>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/revisioncollection/count/) { get; } | Restituisce il numero di revisioni nella raccolta. |
| [Groups](../../aspose.words/revisioncollection/groups/) { get; } | Raccolta di gruppi di revisione. |
| [Item](../../aspose.words/revisioncollection/item/) { get; } | Restituisce un[`Revision`](../revision/) all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Accept](../../aspose.words/revisioncollection/accept/)(*[IRevisionCriteria](../irevisioncriteria/)*) | Accetta le revisioni che corrispondono ai criteri specificati. |
| [AcceptAll](../../aspose.words/revisioncollection/acceptall/)() | Accetta tutte le revisioni in questa raccolta. |
| [GetEnumerator](../../aspose.words/revisioncollection/getenumerator/)() | Restituisce un oggetto enumeratore. |
| [Reject](../../aspose.words/revisioncollection/reject/)(*[IRevisionCriteria](../irevisioncriteria/)*) | Rifiuta le revisioni che corrispondono ai criteri specificati. |
| [RejectAll](../../aspose.words/revisioncollection/rejectall/)() | Rifiuta tutte le revisioni in questa raccolta. |

## Osservazioni

Non creare istanze di questa classe direttamente. Utilizzare il[`Revisions`](../document/revisions/) proprietà per ottenere le revisioni presenti in un documento.

## Esempi

Mostra come lavorare con le revisioni in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La normale modifica del documento non è considerata una revisione.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Per registrare le nostre modifiche come revisioni, dobbiamo dichiarare un autore e poi iniziare a monitorarle.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Questo flag corrisponde all'opzione "Revisione" -> "Monitoraggio" -> "Revisioni" in Microsoft Word.
// Il metodo "StartTrackRevisions" non ne influenza il valore,
// e il documento tiene traccia delle revisioni a livello di programmazione nonostante abbia il valore "false".
// Se apriamo questo documento utilizzando Microsoft Word, le revisioni non verranno monitorate.
Assert.IsFalse(doc.TrackRevisions);

// Abbiamo aggiunto del testo utilizzando il generatore di documenti, quindi la prima revisione è una revisione di tipo inserimento.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Rimuovi un'esecuzione per creare una revisione di tipo eliminazione.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Aggiungendo una nuova revisione, questa viene posizionata all'inizio della raccolta delle revisioni.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Le revisioni inserite vengono visualizzate nel corpo del documento anche prima che accettiamo/rifiutiamo la revisione.
// Rifiutando la revisione, i relativi nodi verranno rimossi dal corpo. Al contrario, i nodi che la compongono elimineranno le revisioni.
// rimangono nel documento finché non accettiamo la revisione.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// L'accettazione della revisione di eliminazione rimuoverà il suo nodo padre dal testo del paragrafo
// e quindi rimuovere la revisione della raccolta stessa.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Ora sposta il nodo per creare un tipo di revisione mobile.
Node node = doc.FirstSection.Body.Paragraphs[1];
Node endNode = doc.FirstSection.Body.Paragraphs[1].NextSibling;
Node referenceNode = doc.FirstSection.Body.Paragraphs[0];

while (node != endNode)
{
    Node nextNode = node.NextSibling;
    doc.FirstSection.Body.InsertBefore(node, referenceNode);
    node = nextNode;
}

Assert.AreEqual(RevisionType.Moving, doc.Revisions[0].RevisionType);
Assert.AreEqual(8, doc.Revisions.Count);
Assert.AreEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.GetText().Trim());

// La revisione in movimento è ora all'indice 1. Rifiutare la revisione per eliminarne il contenuto.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Guarda anche

* class [Revision](../revision/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
