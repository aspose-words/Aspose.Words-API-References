---
title: Bookmark.last_column property
linktitle: last_column property
articleTitle: last_column property
second_title: Aspose.Words for Python
description: "Bookmark.last_column property. Gets the zero-based index of the last column of the table column range associated with the bookmark."
type: docs
weight: 50
url: /de/python-net/aspose.words/bookmark/last_column/
---

## Bookmark.last_column property

Gets the zero-based index of the last column of the table column range associated with the bookmark.


```python
@property
def last_column(self) -> int:
    ...

```

### Remarks

Returns **-1** if this bookmark is not a table column bookmark.



### Examples

Shows how to get information about table column bookmarks.

```python
doc = aw.Document(file_name=MY_DIR + 'Table column bookmarks.doc')
for bookmark in doc.range.bookmarks:
    # Wenn ein Lesezeichen Spalten einer Tabelle umschließt, handelt es sich um ein Tabellenspalten-Lesezeichen, und sein IsColumn-Flag ist auf true gesetzt.
    print(f"Bookmark: {bookmark.name}{(' (Column)' if bookmark.is_column else '')}")
    if bookmark.is_column:
        row = bookmark.bookmark_start.get_ancestor(ancestor_type=aw.NodeType.ROW).as_row()
        if row is not None and bookmark.first_column < row.cells.count:
            # Geben Sie den Inhalt der ersten und letzten Spalten aus, die vom Lesezeichen umschlossen werden.
            print(row.cells[bookmark.first_column].get_text().rstrip(aw.ControlChar.CELL))
            print(row.cells[bookmark.last_column].get_text().rstrip(aw.ControlChar.CELL))
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

