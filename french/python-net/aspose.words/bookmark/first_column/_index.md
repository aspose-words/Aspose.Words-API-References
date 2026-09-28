---
title: Bookmark.first_column property
linktitle: first_column property
articleTitle: first_column property
second_title: Aspose.Words for Python
description: "Bookmark.first_column property. Gets the zero-based index of the first column of the table column range associated with the bookmark."
type: docs
weight: 30
url: /fr/python-net/aspose.words/bookmark/first_column/
---

## Bookmark.first_column property

Gets the zero-based index of the first column of the table column range associated with the bookmark.


```python
@property
def first_column(self) -> int:
    ...

```

### Remarks

Returns **-1** if this bookmark is not a table column bookmark.



### Examples

Shows how to get information about table column bookmarks.

```python
doc = aw.Document(file_name=MY_DIR + 'Table column bookmarks.doc')
for bookmark in doc.range.bookmarks:
    # Si un signet englobe des colonnes d'un tableau, il s'agit d'un signet de colonne de tableau, et son indicateur IsColumn est défini sur true.
    print(f"Bookmark: {bookmark.name}{(' (Column)' if bookmark.is_column else '')}")
    if bookmark.is_column:
        row = bookmark.bookmark_start.get_ancestor(ancestor_type=aw.NodeType.ROW).as_row()
        if row is not None and bookmark.first_column < row.cells.count:
            # Affichez le contenu des première et dernière colonnes englobées par le signet.
            print(row.cells[bookmark.first_column].get_text().rstrip(aw.ControlChar.CELL))
            print(row.cells[bookmark.last_column].get_text().rstrip(aw.ControlChar.CELL))
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

