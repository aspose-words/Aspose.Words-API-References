---
title: DocumentBuilder.delete_row method
linktitle: delete_row method
articleTitle: delete_row method
second_title: Aspose.Words for Python
description: "DocumentBuilder.delete_row method. Deletes a row from a table."
type: docs
weight: 200
url: /python-net/aspose.words/documentbuilder/delete_row/
---

## delete_row(table_index, row_index) {#int_int}

Deletes a row from a table.


```python
def delete_row(self, table_index: int, row_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| table_index | int | The index of the table. |
| row_index | int | The index of the row in the table. |

### Remarks

If the cursor is inside the row that is being deleted, the cursor is moved
out to the next row or to the next paragraph after the table.

If you delete a row from a table that contains only one row, the whole
table is deleted.

For the index parameters, when index is greater than or equal to 0, it specifies an index from
the beginning with 0 being the first element. When index is less than 0, it specified an index from
the end with -1 being the last element.




### Returns

The row node that was just removed.


### Examples

Shows how to delete a row from a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
builder.insert_cell()
builder.write('Row 1, cell 2.')
builder.end_row()
builder.insert_cell()
builder.write('Row 2, cell 1.')
builder.insert_cell()
builder.write('Row 2, cell 2.')
builder.end_table()
self.assertEqual(2, table.rows.count)
# Delete the first row of the first table in the document.
builder.delete_row(0, 0)
self.assertEqual(1, table.rows.count)
self.assertEqual('Row 2, cell 1.\x07Row 2, cell 2.\x07\x07', table.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

