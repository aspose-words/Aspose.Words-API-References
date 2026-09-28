---
title: CellFormat.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for Python
description: "CellFormat.width property. Gets the width of the cell in points."
type: docs
weight: 140
url: /de/python-net/aspose.words.tables/cellformat/width/
---

## CellFormat.width property

Gets the width of the cell in points.


```python
@property
def width(self) -> float:
    ...

@width.setter
def width(self, value: float):
    ...

```

### Remarks

The width is calculated by Aspose.Words on document loading and saving.
Currently, not every combination of table, cell and document properties is supported.
The returned value may not be accurate for some documents.
It may not exactly match the cell width as calculated by MS Word when the document is opened in MS Word.

Setting this property is not recommended.
There is no guarantee that the cell will actually have the set width.
The width may be adjusted to accommodate cell contents in an auto-fit table layout.
Cells in other rows may have conflicting width settings.
The table may be resized to fit into the container or to meet table width settings.
Consider using [CellFormat.preferred_width](../preferred_width/) for setting the cell width.
Setting this property sets [CellFormat.preferred_width](../preferred_width/) implicitly since version 15.8.





### Examples

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
# Festlegen von Tabellenformatierungsoptionen für einen Dokumenten‑Builder
# wird sie auf jede Zeile und Zelle anwenden, die wir damit hinzufügen.
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.cell_format.clear_formatting()
builder.cell_format.width = 150
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.green_yellow
builder.cell_format.wrap_text = False
builder.cell_format.fit_text = True
builder.row_format.clear_formatting()
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.row_format.height = 50
builder.row_format.borders.line_style = aw.LineStyle.ENGRAVE_3D
builder.row_format.borders.color = aspose.pydrawing.Color.orange
builder.insert_cell()
builder.write('Row 1, Col 1')
builder.insert_cell()
builder.write('Row 1, Col 2')
builder.end_row()
# Das Ändern der Formatierung wird sie auf die aktuelle Zelle anwenden,
# und alle neuen Zellen, die wir anschließend mit dem Builder erstellen.
# Dies wird die Zellen, die wir zuvor hinzugefügt haben, nicht beeinflussen.
builder.cell_format.shading.clear_formatting()
builder.insert_cell()
builder.write('Row 2, Col 1')
builder.insert_cell()
builder.write('Row 2, Col 2')
builder.end_row()
# Erhöhen Sie die Zeilenhöhe, um den vertikalen Text anzupassen.
builder.insert_cell()
builder.row_format.height = 150
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write('Row 3, Col 1')
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write('Row 3, Col 2')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTable.docx')
```

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
* property [CellFormat.preferred_width](../preferred_width/)

