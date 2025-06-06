---
title: Bookmark.IsColumn
linktitle: IsColumn
articleTitle: IsColumn
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsColumn. Identifica facilmente se un segnalibro rappresenta una colonna di una tabella, migliorando la navigazione e l'organizzazione dei documenti.
type: docs
weight: 40
url: /it/net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

Restituisce`VERO` se questo segnalibro è un segnalibro di colonna di tabella.

```csharp
public bool IsColumn { get; }
```

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
