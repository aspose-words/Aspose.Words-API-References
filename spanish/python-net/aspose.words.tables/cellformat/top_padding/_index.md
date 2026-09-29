---
title: CellFormat.top_padding property
linktitle: top_padding property
articleTitle: top_padding property
second_title: Aspose.Words for Python
description: "CellFormat.top_padding property. Returns or sets the amount of space (in points) to add above the contents of cell."
type: docs
weight: 110
url: /es/python-net/aspose.words.tables/cellformat/top_padding/
---

## CellFormat.top_padding property

Returns or sets the amount of space (in points) to add above the contents of cell.


```python
@property
def top_padding(self) -> float:
    ...

@top_padding.setter
def top_padding(self, value: float):
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
# Inserte una segunda celda y luego configure las opciones de relleno de texto de la celda.
# El generador aplicará estos ajustes en su celda actual, y cualquier celda nueva creada después.
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
# La primera celda no se vio afectada por la reconfiguración del relleno y aún conserva los valores predeterminados.
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
# La primera celda seguirá creciendo en el documento de salida para coincidir con el tamaño de su celda vecina.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetCellFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

