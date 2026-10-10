---
title: Table.set_borders method
linktitle: set_borders method
articleTitle: set_borders method
second_title: Aspose.Words for Python
description: "Table.set_borders method. Sets all table borders to the specified line style, width and color."
type: docs
weight: 440
url: /sv/python-net/aspose.words.tables/table/set_borders/
---

## set_borders(line_style, line_width, color) {#linestyle_float_color}

Sets all table borders to the specified line style, width and color.


```python
def set_borders(self, line_style: aspose.words.LineStyle, line_width: float, color: aspose.pydrawing.Color):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| line_style | [LineStyle](../../../aspose.words/linestyle/) | The line style to apply. |
| line_width | float | The line width to set (in points). |
| color | aspose.pydrawing.Color | The color to use for the border. |

### Examples

Shows how to apply border and shading color while building a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Starta en tabell och ange en standardfärg/tjocklek för dess kanter.
table = builder.start_table()
table.set_borders(aw.LineStyle.SINGLE, 2, aspose.pydrawing.Color.black)
# Skapa en rad med två celler med olika bakgrundsfärger.
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_sky_blue
builder.writeln('Row 1, Cell 1.')
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.orange
builder.writeln('Row 1, Cell 2.')
builder.end_row()
# Återställ cellformatering för att inaktivera bakgrundsfärgerna
# ange en anpassad kanttjocklek för alla nya celler som skapas av byggaren,
# bygg sedan en andra rad.
builder.cell_format.clear_formatting()
builder.cell_format.borders.left.line_width = 4
builder.cell_format.borders.right.line_width = 4
builder.cell_format.borders.top.line_width = 4
builder.cell_format.borders.bottom.line_width = 4
builder.insert_cell()
builder.writeln('Row 2, Cell 1.')
builder.insert_cell()
builder.writeln('Row 2, Cell 2.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.TableBordersAndShading.docx')
```

Shows how to format of all of a table's borders at once.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# Rensa alla befintliga kanter från tabellen.
table.clear_borders()
# Ställ in en enda grön linje som både yttre och inre kant för denna tabell.
table.set_borders(aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green)
doc.save(file_name=ARTIFACTS_DIR + 'Table.SetBorders.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

