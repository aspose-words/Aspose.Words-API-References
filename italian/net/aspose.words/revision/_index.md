---
title: Class Revision
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Revision classe. Rappresenta una revisione modifica tracciata in un nodo o stile di documento. UtilizzoRevisionType per verificare il tipo di questa revisione.
type: docs
weight: 4760
url: /it/net/aspose.words/revision/
---
## Revision class

Rappresenta una revisione (modifica tracciata) in un nodo o stile di documento. Utilizzo[`RevisionType`](./revisiontype/) per verificare il tipo di questa revisione.

Per saperne di più, visita il[Tieni traccia delle modifiche in un documento](https://docs.aspose.com/words/net/track-changes-in-a-document/) articolo di documentazione.

```csharp
public class Revision
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | Ottiene o imposta l'autore di questa revisione. Non può essere una stringa vuota o`nullo` . |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | Ottiene o imposta la data/ora di questa revisione. |
| [Group](../../aspose.words/revision/group/) { get; } | Ottiene il gruppo di revisione. ritorna`nullo` se la revisione non appartiene a nessun gruppo. |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | Ottiene il nodo padre immediato (proprietario) di questa revisione. Questa proprietà funzionerà per qualsiasi tipo di revisione diverso daStyleDefinitionChange . |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | Ottiene lo stile principale immediato (proprietario) di questa revisione. Questa proprietà funzionerà solo perStyleDefinitionChange tipo di revisione. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | Ottiene il tipo di questa revisione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Accept](../../aspose.words/revision/accept/)() | Accetta questa revisione. |
| [Reject](../../aspose.words/revision/reject/)() | Rifiuta questa revisione. |

### Esempi

Mostra come lavorare con le revisioni in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La normale modifica del documento non conta come una revisione.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Per registrare le nostre modifiche come revisioni, dobbiamo dichiarare un autore e quindi iniziare a monitorarle.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Questo flag corrisponde alla "Revisione" -> "Tracciamento" -> Opzione "Traccia modifiche" in Microsoft Word.
// Il metodo "StartTrackRevisions" non influisce sul suo valore,
// e il documento tiene traccia delle revisioni a livello di codice nonostante abbia il valore "false".
// Se apriamo questo documento utilizzando Microsoft Word, non verranno monitorate le revisioni.
Assert.IsFalse(doc.TrackRevisions);

// Abbiamo aggiunto del testo utilizzando il generatore di documenti, quindi la prima revisione è una revisione di tipo inserimento.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Rimuove un'esecuzione per creare una revisione di tipo eliminazione.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// L'aggiunta di una nuova revisione la posiziona all'inizio della raccolta di revisioni.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Le revisioni inserite vengono visualizzate nel corpo del documento anche prima di accettare/rifiutare la revisione.
// Rifiutare la revisione rimuoverà i suoi nodi dal corpo. Al contrario, i nodi che compongono eliminano le revisioni
// rimaniamo anche nel documento finché non accettiamo la revisione.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Accettando la revisione di eliminazione rimuoverà il suo nodo principale dal testo del paragrafo
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

// La revisione in movimento è ora all'indice 1. Rifiuta la revisione per scartarne il contenuto.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


