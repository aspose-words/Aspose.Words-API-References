---
title: Bookmark.is_column property
linktitle: is_column property
articleTitle: is_column property
second_title: Aspose.Words for Python
description: "Bookmark.is_column property. Returns ``True`` if this bookmark is a table column bookmark."
type: docs
weight: 40
url: /python-net/aspose.words/bookmark/is_column/
---

## Bookmark.is_column property

Returns ``True`` if this bookmark is a table column bookmark.



```python
@property
def is_column(self) -> bool:
    ...

```

### Examples

Shows how to get information about table column bookmarks.

```python
doc = aw.Document(file_name=MY_DIR + 'Table column bookmarks.doc')
for bookmark in doc.range.bookmarks:
    # If a bookmark encloses columns of a table, it is a table column bookmark, and its IsColumn flag set to true.
    print(f"Bookmark: {bookmark.name}{(' (Column)' if bookmark.is_column else '')}")
    if bookmark.is_column:
        row = bookmark.bookmark_start.get_ancestor(ancestor_type=aw.NodeType.ROW).as_row()
        if row is not None and bookmark.first_column < row.cells.count:
            # Print the contents of the first and last columns enclosed by the bookmark.
            print(row.cells[bookmark.first_column].get_text().rstrip(aw.ControlChar.CELL))
            print(row.cells[bookmark.last_column].get_text().rstrip(aw.ControlChar.CELL))
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

