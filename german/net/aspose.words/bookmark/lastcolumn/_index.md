---
title: Bookmark.LastColumn
linktitle: LastColumn
articleTitle: LastColumn
second_title: Aspose.Words für .NET
description: Entdecken Sie die LastColumn-Eigenschaft und greifen Sie für eine effiziente Datenverwaltung einfach auf den nullbasierten Index der letzten Spalte im Lesezeichenbereich Ihrer Tabelle zu.
type: docs
weight: 50
url: /de/net/aspose.words/bookmark/lastcolumn/
---
## Bookmark.LastColumn property

Ruft den nullbasierten Index der letzten Spalte des Tabellenspaltenbereichs ab, der dem Lesezeichen zugeordnet ist.

```csharp
public int LastColumn { get; }
```

## Bemerkungen

Rückgaben**-1** wenn dieses Lesezeichen kein Tabellenspalten-Lesezeichen ist.

## Beispiele

Zeigt, wie Informationen zu Tabellenspalten-Lesezeichen abgerufen werden.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Wenn ein Lesezeichen Spalten einer Tabelle umschließt, handelt es sich um ein Tabellenspalten-Lesezeichen und sein IsColumn-Flag ist auf „true“ gesetzt.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Druckt den Inhalt der ersten und letzten Spalte, die vom Lesezeichen umschlossen werden.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### Siehe auch

* class [Bookmark](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
