---
title: Bookmark.IsColumn
linktitle: IsColumn
articleTitle: IsColumn
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsColumn-Eigenschaft. Erkennen Sie mühelos, ob ein Lesezeichen eine Tabellenspalte darstellt, und verbessern Sie so die Navigation und Organisation Ihrer Dokumente.
type: docs
weight: 40
url: /de/net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

Rückgaben`WAHR` wenn dieses Lesezeichen ein Tabellenspalten-Lesezeichen ist.

```csharp
public bool IsColumn { get; }
```

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
