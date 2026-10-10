---
title: CellFormat.top_padding property
linktitle: top_padding property
articleTitle: top_padding property
second_title: Aspose.Words for Python
description: "CellFormat.top_padding property. Returns or sets the amount of space (in points) to add above the contents of cell."
type: docs
weight: 110
url: /de/python-net/aspose.words.tables/cellformat/top_padding/
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

