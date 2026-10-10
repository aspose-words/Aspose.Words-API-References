---
title: CellFormat.left_padding property
linktitle: left_padding property
articleTitle: left_padding property
second_title: Aspose.Words for Python
description: "CellFormat.left_padding property. Returns or sets the amount of space (in points) to add to the left of the contents of cell."
type: docs
weight: 60
url: /de/python-net/aspose.words.tables/cellformat/left_padding/
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
# Fügen Sie eine zweite Zelle ein und konfigurieren Sie dann die Optionen für die Zelltext‑Einrückung.
# Der Builder wendet diese Einstellungen auf seine aktuelle Zelle an, und alle neu erstellten Zellen danach übernehmen sie.
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
# Die erste Zelle blieb von der Neu­konfiguration der Einrückung unberührt und behält weiterhin die Standardwerte.
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
# Die erste Zelle wird im Ausgabedokument weiterhin wachsen, um die Größe ihrer benachbarten Zelle anzupassen.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetCellFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

