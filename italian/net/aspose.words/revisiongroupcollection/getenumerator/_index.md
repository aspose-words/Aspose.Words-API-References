---
title: RevisionGroupCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words per .NET
description: Scopri il metodo GetEnumerator di RevisionGroupCollection: recupera in modo efficiente gli oggetti enumeratori per una gestione semplificata dei dati e prestazioni migliorate.
type: docs
weight: 30
url: /it/net/aspose.words/revisiongroupcollection/getenumerator/
---
## RevisionGroupCollection.GetEnumerator method

Restituisce un oggetto enumeratore.

```csharp
public IEnumerator<RevisionGroup> GetEnumerator()
```

## Esempi

Mostra come lavorare con la raccolta di revisioni di un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Questa raccolta contiene a sua volta una raccolta di gruppi di revisione.
// Ogni gruppo è una sequenza di revisioni adiacenti.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Esegui l'iterazione sulla raccolta di gruppi e stampa il testo a cui si riferisce la revisione.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Ogni esecuzione interessata da una revisione ottiene un oggetto Revision corrispondente.
// La raccolta delle revisioni è considerevolmente più grande della forma condensata che abbiamo stampato sopra,
// a seconda del numero di Esecuzioni in cui abbiamo segmentato il documento durante la modifica in Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // Un StyleDefinitionChange influenza esclusivamente gli stili e non i nodi del documento. Questo significa che "ParentStyle"
        // la proprietà sarà sempre in uso, mentre ParentNode sarà sempre null.
        // Poiché tutte le altre modifiche interessano i nodi, verrà invece utilizzato ParentNode e ParentStyle sarà null.
        if (e.Current.RevisionType == RevisionType.StyleDefinitionChange)
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, style: [{e.Current.ParentStyle.Name}]");
        }
        else
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, contents: [{e.Current.ParentNode.GetText().Trim()}]");
        }
    }
}

// Rifiuta tutte le revisioni tramite la raccolta, ripristinando il documento nella sua forma originale.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Guarda anche

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
