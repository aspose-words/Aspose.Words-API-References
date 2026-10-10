---
title: Table.clear_borders method
linktitle: clear_borders method
articleTitle: clear_borders method
second_title: Aspose.Words for Python
description: "Table.clear_borders method. Removes all table and cell borders on this table."
type: docs
weight: 390
url: /sv/python-net/aspose.words.tables/table/clear_borders/
---

## clear_borders() {#default}

Removes all table and cell borders on this table.


```python
def clear_borders(self):
    ...
```

### Examples

Shows how to apply an outline border to a table.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# Justera tabellen till mitten av sidan.
table.alignment = aw.tables.TableAlignment.CENTER
# Rensa eventuella befintliga kanter och skuggning från tabellen.
table.clear_borders()
table.clear_shading()
# Lägg till gröna kanter runt tabellens kontur.
table.set_border(aw.BorderType.LEFT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.RIGHT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.TOP, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.BOTTOM, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
# Fyll cellerna med en ljusgrön solid färg.
table.set_shading(aw.TextureIndex.TEXTURE_SOLID, aspose.pydrawing.Color.light_green, aspose.pydrawing.Color.empty())
doc.save(file_name=ARTIFACTS_DIR + 'Table.SetOutlineBorders.docx')
```

Shows how to remove all borders from a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Hello world!')
builder.end_table()
# Ändra färgen och tjockleken på den övre kanten.
top_border = table.first_row.row_format.borders.get_by_border_type(aw.BorderType.TOP)
table.set_border(aw.BorderType.TOP, aw.LineStyle.DOUBLE, 1.5, aspose.pydrawing.Color.red, True)
self.assertEqual(1.5, top_border.line_width)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), top_border.color.to_argb())
self.assertEqual(aw.LineStyle.DOUBLE, top_border.line_style)
# Rensa kanterna på alla celler i tabellen och spara sedan dokumentet.
table.clear_borders()
doc.save(file_name=ARTIFACTS_DIR + 'Table.ClearBorders.docx')
# Verifiera värdena för tabellens egenskaper efter att ha öppnat dokumentet igen.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Table.ClearBorders.docx')
table = doc.first_section.body.tables[0]
top_border = table.first_row.row_format.borders.get_by_border_type(aw.BorderType.TOP)
self.assertEqual(0, top_border.line_width)
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), top_border.color.to_argb())
self.assertEqual(aw.LineStyle.NONE, top_border.line_style)
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

