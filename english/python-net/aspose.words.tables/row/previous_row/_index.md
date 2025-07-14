---
title: Row.previous_row property
linktitle: previous_row property
articleTitle: previous_row property
second_title: Aspose.Words for Python
description: "Row.previous_row property. Gets the previous [Row](../) node."
type: docs
weight: 110
url: /python-net/aspose.words.tables/row/previous_row/
---

## Row.previous_row property

Gets the previous [Row](../) node.



```python
@property
def previous_row(self) -> aspose.words.tables.Row:
    ...

```

### Remarks

The method can be used when you need to have typed access to table rows. If a
[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node is found in a table instead of a row,
it is automatically traversed to get a row contained within.



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
* class [Row](../)

