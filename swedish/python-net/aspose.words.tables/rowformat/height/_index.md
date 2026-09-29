---
title: RowFormat.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for Python
description: "RowFormat.height property. Gets or sets the height of the table row in points."
type: docs
weight: 40
url: /sv/python-net/aspose.words.tables/rowformat/height/
---

## RowFormat.height property

Gets or sets the height of the table row in points.


```python
@property
def height(self) -> float:
    ...

@height.setter
def height(self, value: float):
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
# Ställ in några formateringsalternativ för text- och tabellutseende.
builder.row_format.height = 40
builder.row_format.height_rule = aw.HeightRule.AT_LEAST
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.from_argb(198, 217, 241)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.font.size = 16
builder.font.name = 'Arial'
builder.font.bold = True
# Att konfigurera formateringsalternativen i en dokumentbyggare kommer att tillämpa dem
# på den aktuella cellen/raden som dess markör befinner sig i,
# samt alla nya celler och rader som skapas med den byggaren.
builder.write('Header Row,\n Cell 1')
builder.insert_cell()
builder.write('Header Row,\n Cell 2')
builder.insert_cell()
builder.write('Header Row,\n Cell 3')
builder.end_row()
# Omkonfigurera byggarens formateringsobjekt för nya rader och celler som vi är på väg att skapa.
# Byggaren kommer inte att tillämpa dessa på den första redan skapade raden så att den framträder som en rubrikrad.
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
# Starta en andra rad och konfigurera sedan dess höjd. Byggaren kommer att tillämpa dessa inställningar på
# dess nuvarande rad, samt eventuella nya rader den skapar därefter.
builder.end_row()
row_format = builder.row_format
row_format.height = 100
row_format.height_rule = aw.HeightRule.EXACTLY
builder.insert_cell()
builder.write('Row 2, cell 1.')
builder.end_table()
# Den första raden påverkades inte av omkonfigurationen av utfyllnad och behåller fortfarande standardvärdena.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetRowFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [RowFormat](../)

