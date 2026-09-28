---
title: RowFormat.borders property
linktitle: borders property
articleTitle: borders property
second_title: Aspose.Words for Python
description: "RowFormat.borders property. Gets the collection of default cell borders for the row."
type: docs
weight: 20
url: /de/python-net/aspose.words.tables/rowformat/borders/
---

## RowFormat.borders property

Gets the collection of default cell borders for the row.


```python
@property
def borders(self) -> aspose.words.BorderCollection:
    ...

```

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

### See Also

* module [aspose.words.tables](../../)
* class [RowFormat](../)

