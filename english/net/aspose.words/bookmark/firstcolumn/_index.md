---
title: Bookmark.FirstColumn
second_title: Aspose.Words for .NET API Reference
description: Bookmark property. Gets the zerobased index of the first column of the table column range associated with the bookmark in C#.
type: docs
weight: 30
url: /net/aspose.words/bookmark/firstcolumn/
---
## Bookmark.FirstColumn property

Gets the zero-based index of the first column of the table column range associated with the bookmark.

```csharp
public int FirstColumn { get; }
```

## Remarks

Returns **-1** if this bookmark is not a table column bookmark.

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
* namespace [Aspose.Words](../../bookmark/)
* assembly [Aspose.Words](../../../)
