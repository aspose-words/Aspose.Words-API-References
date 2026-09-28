---
title: RowFormat.height_rule property
linktitle: height_rule property
articleTitle: height_rule property
second_title: Aspose.Words for Python
description: "RowFormat.height_rule property. Gets or sets the rule for determining the height of the table row."
type: docs
weight: 50
url: /de/python-net/aspose.words.tables/rowformat/height_rule/
---

## RowFormat.height_rule property

Gets or sets the rule for determining the height of the table row.


```python
@property
def height_rule(self) -> aspose.words.HeightRule:
    ...

@height_rule.setter
def height_rule(self, value: aspose.words.HeightRule):
    ...

```

### Examples

Shows how to create a formatted table using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
table.left_indent = 20
# Lege einige Formatierungsoptionen für Text- und Tabellenanzeige fest.
builder.row_format.height = 40
builder.row_format.height_rule = aw.HeightRule.AT_LEAST
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.from_argb(198, 217, 241)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.font.size = 16
builder.font.name = 'Arial'
builder.font.bold = True
# Das Konfigurieren der Formatierungsoptionen in einem Dokument-Builder wendet sie an
# auf die aktuelle Zelle/Zeile, in der sich sein Cursor befindet,
# sowie auf alle neuen Zellen und Zeilen, die mit diesem Builder erstellt werden.
builder.write('Header Row,\n Cell 1')
builder.insert_cell()
builder.write('Header Row,\n Cell 2')
builder.insert_cell()
builder.write('Header Row,\n Cell 3')
builder.end_row()
# Konfiguriere die Formatierungsobjekte des Builders neu für neue Zeilen und Zellen, die wir gleich erstellen werden.
# Der Builder wird diese nicht auf die bereits erstellte erste Zeile anwenden, damit sie als Kopfzeile hervorsticht.
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.white
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.row_format.height = 30
builder.row_format.height_rule = aw.HeightRule.AUTO
builder.insert_cell()
builder.font.size = 12
builder.font.bold = False
builder.write('Row 1, Cell 1.')
builder.insert_cell()
builder.write('Row 1, Cell 2.')
builder.insert_cell()
builder.write('Row 1, Cell 3.')
builder.end_row()
builder.insert_cell()
builder.write('Row 2, Cell 1.')
builder.insert_cell()
builder.write('Row 2, Cell 2.')
builder.insert_cell()
builder.write('Row 2, Cell 3.')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.CreateFormattedTable.docx')
```

Shows how to format rows with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
# Starte eine zweite Zeile und konfiguriere anschließend deren Höhe. Der Builder wird diese Einstellungen anwenden auf
# seine aktuelle Zeile sowie alle neuen Zeilen, die er anschließend erstellt.
builder.end_row()
row_format = builder.row_format
row_format.height = 100
row_format.height_rule = aw.HeightRule.EXACTLY
builder.insert_cell()
builder.write('Row 2, cell 1.')
builder.end_table()
# Die erste Zeile war von der Neukonfiguration des Paddings unbeeinflusst und enthält weiterhin die Standardwerte.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetRowFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [RowFormat](../)

