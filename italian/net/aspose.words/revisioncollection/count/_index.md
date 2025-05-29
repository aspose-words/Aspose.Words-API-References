---
title: RevisionCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà RevisionCollection Count, che rivela in modo efficiente il numero totale di revisioni, migliorando la gestione e il monitoraggio dei dati.
type: docs
weight: 10
url: /it/net/aspose.words/revisioncollection/count/
---
## RevisionCollection.Count property

Restituisce il numero di revisioni nella raccolta.

```csharp
public int Count { get; }
```

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

* class [RevisionCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
