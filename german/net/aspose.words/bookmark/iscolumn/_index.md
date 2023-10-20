---
title: Bookmark.IsColumn
linktitle: IsColumn
articleTitle: IsColumn
second_title: Aspose.Words für .NET
description: Bookmark IsColumn eigendom. Gibt zurückWAHR wenn dieses Lesezeichen ein TabellenspaltenLesezeichen ist in C#.
type: docs
weight: 40
url: /de/net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

Gibt zurück`WAHR` wenn dieses Lesezeichen ein Tabellenspalten-Lesezeichen ist.

```csharp
public bool IsColumn { get; }
```

## Beispiele

Zeigt, wie Sie Informationen zu Tabellenspalten-Lesezeichen erhalten.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Wenn ein Lesezeichen Spalten einer Tabelle einschließt, handelt es sich um ein Tabellenspalten-Lesezeichen und sein IsColumn-Flag ist auf „true“ gesetzt.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Den Inhalt der ersten und letzten Spalte drucken, die vom Lesezeichen eingeschlossen sind.
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
