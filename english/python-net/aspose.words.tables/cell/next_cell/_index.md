---
title: Cell.next_cell property
linktitle: next_cell property
articleTitle: next_cell property
second_title: Aspose.Words for Python
description: "Cell.next_cell property. Gets the next [Cell](../) node."
type: docs
weight: 70
url: /python-net/aspose.words.tables/cell/next_cell/
---

## Cell.next_cell property

Gets the next [Cell](../) node.



```python
@property
def next_cell(self) -> aspose.words.tables.Cell:
    ...

```

### Remarks

The method can be used when you need to have typed access to cells of a [Row](../../row/). If a
[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node is found in a row instead of a cell, it is automatically
traversed to get a cell contained within.



### Examples

Shows how to enumerate through all table cells.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# Enumerate through all cells of the table.
row = table.first_row
while row != None:
    cell = row.first_cell
    while cell != None:
        print(cell.get_text())
        cell = cell.next_cell
    row = row.next_row
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

