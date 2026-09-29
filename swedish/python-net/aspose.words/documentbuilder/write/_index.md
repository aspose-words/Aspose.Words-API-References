---
title: DocumentBuilder.write method
linktitle: write method
articleTitle: write method
second_title: Aspose.Words for Python
description: "DocumentBuilder.write method. Inserts a string into the document at the current insert position."
type: docs
weight: 690
url: /sv/python-net/aspose.words/documentbuilder/write/
---

## write(text) {#str}

Inserts a string into the document at the current insert position.


```python
def write(self, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | str | The string to insert into the document. |

### Remarks

Current font formatting specified by the [DocumentBuilder.font](../font/) property is used.



### Examples

Shows how to insert a string surrounded by a border into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.border.color = aspose.pydrawing.Color.green
builder.font.border.line_width = 2.5
builder.font.border.line_style = aw.LineStyle.DASH_DOT_STROKER
builder.write('Text surrounded by green border.')
doc.save(file_name=ARTIFACTS_DIR + 'Border.FontBorder.docx')
```

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
# Ställa in tabellformateringsalternativ för en dokumentbyggare
# kommer att tillämpa dem på varje rad och cell som vi lägger till med den.
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
# Att ändra formateringen kommer att tillämpa den på den aktuella cellen,
# och alla nya celler som vi skapar med byggaren efteråt.
# Detta kommer inte att påverka de celler som vi har lagt till tidigare.
builder.cell_format.shading.clear_formatting()
builder.insert_cell()
builder.write('Row 2, Col 1')
builder.insert_cell()
builder.write('Row 2, Col 2')
builder.end_row()
# Öka radhöjden så att den passar den vertikala texten.
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

Shows how to use a document builder to create a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Starta tabellen och fyll sedan den första raden med två celler.
builder.start_table()
builder.insert_cell()
builder.write('Row 1, Cell 1.')
builder.insert_cell()
builder.write('Row 1, Cell 2.')
# Anropa byggarens "EndRow"-metod för att starta en ny rad.
builder.end_row()
builder.insert_cell()
builder.write('Row 2, Cell 1.')
builder.insert_cell()
builder.write('Row 2, Cell 2.')
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.CreateTable.docx')
```

Shows how to build a formatted 2x2 table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.write('Row 1, cell 1.')
builder.insert_cell()
builder.write('Row 1, cell 2.')
builder.end_row()
# När tabellen byggs kommer dokumentbyggaren att tillämpa sina aktuella RowFormat/CellFormat-egenskapsvärden
# på den aktuella raden/cellen där dess markör befinner sig samt på alla nya rader/celler när de skapas.
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
# Tidigare tillagda rader och celler påverkas inte retroaktivt av förändringar i byggarens formatering.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
self.assertEqual(aw.TextOrientation.UPWARD, table.rows[1].cells[0].cell_format.orientation)
self.assertEqual(aw.TextOrientation.DOWNWARD, table.rows[1].cells[1].cell_format.orientation)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.BuildTable.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

