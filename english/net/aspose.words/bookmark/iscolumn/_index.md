---
title: Bookmark.IsColumn
linktitle: IsColumn
articleTitle: IsColumn
second_title: Aspose.Words for .NET
description: Discover the IsColumn property: Easily identify if a bookmark represents a table column, enhancing your document navigation and organization.
type: docs
weight: 40
url: /net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

Returns `true` if this bookmark is a table column bookmark.

```csharp
public bool IsColumn { get; }
```

## Examples

Shows how to get information about table column bookmarks.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // If a bookmark encloses columns of a table, it is a table column bookmark, and its IsColumn flag set to true.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Print the contents of the first and last columns enclosed by the bookmark.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### See Also

* class [Bookmark](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
