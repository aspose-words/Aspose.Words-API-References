---
title: DocumentBuilder.move_to_cell method
linktitle: move_to_cell method
articleTitle: move_to_cell method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_cell method. Moves the cursor to a table cell in the current section."
type: docs
weight: 540
url: /python-net/aspose.words/documentbuilder/move_to_cell/
---

## move_to_cell(table_index, row_index, column_index, character_index) {#int_int_int_int}

Moves the cursor to a table cell in the current section.


```python
def move_to_cell(self, table_index: int, row_index: int, column_index: int, character_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| table_index | int | The index of the table to move to. |
| row_index | int | The index of the row in the table. |
| column_index | int | The index of the column in the table. |
| character_index | int | The index of the character inside the cell. A negative value allows you to specify a position from the end of the cell. Use -1 to move to the end of the cell. |

### Remarks

The navigation is performed inside the current story of the current section.

For the index parameters, when index is greater than or equal to 0, it specifies an index from
the beginning with 0 being the first element. When index is less than 0, it specified an index from
the end with -1 being the last element.




### Examples

Shows how to move a document builder's cursor to a cell in a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Create an empty 2x2 table.
builder.start_table()
builder.insert_cell()
builder.insert_cell()
builder.end_row()
builder.insert_cell()
builder.insert_cell()
builder.end_table()
# Because we have ended the table with the EndTable method,
# the document builder's cursor is currently outside the table.
# This cursor has the same function as Microsoft Word's blinking text cursor.
# It can also be moved to a different location in the document using the builder's MoveTo methods.
# We can move the cursor back inside the table to a specific cell.
builder.move_to_cell(0, 1, 1, 0)
builder.write('Column 2, cell 2.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.MoveToCell.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

