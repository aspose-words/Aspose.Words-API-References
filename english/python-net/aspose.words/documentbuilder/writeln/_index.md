---
title: DocumentBuilder.writeln method
linktitle: writeln method
articleTitle: writeln method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.writeln method"
type: docs
weight: 670
url: /python-net/aspose.words/documentbuilder/writeln/
---

## writeln(text) {#str}

Inserts a string and a paragraph break into the document.


```python
def writeln(self, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | str | The string to insert into the document. |

### Remarks

Current font and paragraph formatting specified by the [DocumentBuilder.font](../font/) and [DocumentBuilder.paragraph_format](../paragraph_format/) properties are used.



## writeln() {#default}

Inserts a paragraph break into the document.


```python
def writeln(self):
    ...
```

### Remarks

Calls [DocumentBuilder.insert_paragraph()](../insert_paragraph/#default).




## Examples

Shows how to build a formatted 2x2 table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
table = builder.start_table()
builder.insert_cell()
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.write('Row 1, cell 1.')
builder.insert_cell()
builder.write('Row 1, cell 2.')
builder.end_row()
# While building the table, the document builder will apply its current RowFormat/CellFormat property values
# to the current row/cell that its cursor is in and any new rows/cells as it creates them.
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[0].cell_format.vertical_alignment)
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[1].cell_format.vertical_alignment)
builder.insert_cell()
builder.row_format.height = 100
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write('Row 2, cell 1.')
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write('Row 2, cell 2.')
builder.end_row()
builder.end_table()
# Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
self.assertEqual(aw.TextOrientation.UPWARD, table.rows[1].cells[0].cell_format.orientation)
self.assertEqual(aw.TextOrientation.DOWNWARD, table.rows[1].cells[1].cell_format.orientation)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.BuildTable.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

