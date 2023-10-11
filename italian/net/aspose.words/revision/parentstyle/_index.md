---
title: Revision.ParentStyle
second_title: Aspose.Words per .NET API Reference
description: Revision proprietà. Ottiene lo stile principale immediato proprietario di questa revisione. Questa proprietà funzionerà solo perStyleDefinitionChange tipo di revisione.
type: docs
weight: 50
url: /it/net/aspose.words/revision/parentstyle/
---
## Revision.ParentStyle property

Ottiene lo stile principale immediato (proprietario) di questa revisione. Questa proprietà funzionerà solo perStyleDefinitionChange tipo di revisione.

```csharp
public Style ParentStyle { get; }
```

### Osservazioni

Se questa revisione si riferisce a modifiche sui nodi del documento, utilizzare[`ParentNode`](../parentnode/) invece.

### Esempi

Mostra come lavorare con la raccolta di revisioni di un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Questa raccolta stessa contiene una raccolta di gruppi di revisione.
// Ogni gruppo è una sequenza di revisioni adiacenti.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Itera sulla raccolta di gruppi e stampa il testo interessato dalla revisione.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Ogni esecuzione interessata da una revisione ottiene un oggetto Revision corrispondente.
// La raccolta delle revisioni è notevolmente più grande della forma ridotta che abbiamo stampato sopra,
// a seconda del numero di sequenze in cui abbiamo segmentato il documento durante la modifica di Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // Uno StyleDefinitionChange influisce strettamente sugli stili e non sui nodi del documento. Ciò significa "ParentStyle"
        // la proprietà sarà sempre in uso, mentre ParentNode sarà sempre null.
        // Poiché tutte le altre modifiche influiscono sui nodi, ParentNode sarà al contrario in uso e ParentStyle sarà nullo.
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

// Rifiuta tutte le revisioni tramite la raccolta, riportando il documento alla sua forma originale.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Guarda anche

* class [Style](../../style/)
* class [Revision](../)
* spazio dei nomi [Aspose.Words](../../revision/)
* assemblea [Aspose.Words](../../../)


