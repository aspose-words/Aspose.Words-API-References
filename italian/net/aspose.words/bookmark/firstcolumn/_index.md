---
title: Bookmark.FirstColumn
linktitle: FirstColumn
articleTitle: FirstColumn
second_title: Aspose.Words per .NET
description: Scopri la proprietà FirstColumn. Accedi facilmente all'indice a partire da zero della prima colonna nell'intervallo di segnalibri della tua tabella per una gestione efficiente dei dati.
type: docs
weight: 30
url: /it/net/aspose.words/bookmark/firstcolumn/
---
## Bookmark.FirstColumn property

Ottiene l'indice basato su zero della prima colonna dell'intervallo di colonne della tabella associato al segnalibro.

```csharp
public int FirstColumn { get; }
```

## Osservazioni

Restituisce**-1** se questo segnalibro non è un segnalibro di colonna di tabella.

## Esempi

Mostra come ottenere informazioni sui segnalibri delle colonne della tabella.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Se un segnalibro racchiude colonne di una tabella, si tratta di un segnalibro di colonna di tabella e il suo flag IsColumn è impostato su true.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Stampa il contenuto della prima e dell'ultima colonna racchiuse dal segnalibro.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### Guarda anche

* class [Bookmark](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
