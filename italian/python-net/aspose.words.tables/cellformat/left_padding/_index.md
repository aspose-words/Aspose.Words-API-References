---
title: CellFormat.left_padding property
linktitle: left_padding property
articleTitle: left_padding property
second_title: Aspose.Words for Python
description: "CellFormat.left_padding property. Returns or sets the amount of space (in points) to add to the left of the contents of cell."
type: docs
weight: 60
url: /it/python-net/aspose.words.tables/cellformat/left_padding/
---

## CellFormat.left_padding property

Returns or sets the amount of space (in points) to add to the left of the contents of cell.


```python
@property
def left_padding(self) -> float:
    ...

@left_padding.setter
def left_padding(self, value: float):
    ...

```

### Examples

Shows how to format cells with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
# Inserisci una seconda cella e poi configura le opzioni di padding del testo della cella.
# Il builder applicherà queste impostazioni alla cella corrente e qualsiasi nuova cella creata successivamente.
builder.insert_cell()
cell_format = builder.cell_format
cell_format.width = 250
cell_format.left_padding = 30
cell_format.right_padding = 30
cell_format.top_padding = 30
cell_format.bottom_padding = 30
builder.write('Row 1, cell 2.')
builder.end_row()
builder.end_table()
# La prima cella non è stata influenzata dalla riconfigurazione del padding e mantiene ancora i valori predefiniti.
self.assertEqual(0, table.first_row.cells[0].cell_format.width)
self.assertEqual(5.4, table.first_row.cells[0].cell_format.left_padding)
self.assertEqual(5.4, table.first_row.cells[0].cell_format.right_padding)
self.assertEqual(0, table.first_row.cells[0].cell_format.top_padding)
self.assertEqual(0, table.first_row.cells[0].cell_format.bottom_padding)
self.assertEqual(250, table.first_row.cells[1].cell_format.width)
self.assertEqual(30, table.first_row.cells[1].cell_format.left_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.right_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.top_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.bottom_padding)
# La prima cella crescerà comunque nel documento di output per corrispondere alle dimensioni della cella adiacente.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetCellFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

