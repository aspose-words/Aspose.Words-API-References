---
title: Bookmark.FirstColumn
second_title: Aspose.Words für .NET-API-Referenz
description: Bookmark eigendom. Ruft den nullbasierten Index der ersten Spalte des Tabellenspaltenbereichs ab der dem Lesezeichen zugeordnet ist.
type: docs
weight: 30
url: /de/net/aspose.words/bookmark/firstcolumn/
---
## Bookmark.FirstColumn property

Ruft den nullbasierten Index der ersten Spalte des Tabellenspaltenbereichs ab, der dem Lesezeichen zugeordnet ist.

```csharp
public int FirstColumn { get; }
```

### Bemerkungen

gibt zurück **-1** wenn dieses Lesezeichen kein Tabellenspalten-Lesezeichen ist.

### Beispiele

Zeigt, wie Informationen zu Tabellenspalten-Lesezeichen abgerufen werden.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Wenn ein Lesezeichen Spalten einer Tabelle umschließt, ist es ein Tabellenspalten-Lesezeichen und sein IsColumn-Flag ist auf wahr gesetzt.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Gibt den Inhalt der ersten und letzten Spalte aus, die vom Lesezeichen eingeschlossen sind.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### Siehe auch

* class [Bookmark](../)
* namensraum [Aspose.Words](../../bookmark/)
* Montage [Aspose.Words](../../../)


