---
title: Bookmark.last_column property
linktitle: last_column property
articleTitle: last_column property
second_title: Aspose.Words for Python
description: "Bookmark.last_column property. Gets the zero-based index of the last column of the table column range associated with the bookmark."
type: docs
weight: 50
url: /zh/python-net/aspose.words/bookmark/last_column/
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
    # 如果书签包围表格的列，则它是表列书签，并将其 IsColumn 标志设置为 true。
    print(f"Bookmark: {bookmark.name}{(' (Column)' if bookmark.is_column else '')}")
    if bookmark.is_column:
        row = bookmark.bookmark_start.get_ancestor(ancestor_type=aw.NodeType.ROW).as_row()
        if row is not None and bookmark.first_column < row.cells.count:
            # 打印书签包围的第一列和最后一列的内容。
            print(row.cells[bookmark.first_column].get_text().rstrip(aw.ControlChar.CELL))
            print(row.cells[bookmark.last_column].get_text().rstrip(aw.ControlChar.CELL))
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

