---
title: Table.cell_spacing property
linktitle: cell_spacing property
articleTitle: cell_spacing property
second_title: Aspose.Words for Python
description: "Table.cell_spacing property. Gets or sets the amount of space (in points) between the cells."
type: docs
weight: 100
url: /es/python-net/aspose.words.tables/table/cell_spacing/
---

## Table.cell_spacing property

Gets or sets the amount of space (in points) between the cells.


```python
@property
def cell_spacing(self) -> float:
    ...

@cell_spacing.setter
def cell_spacing(self, value: float):
    ...

```

### Examples

Shows how to enable spacing between individual cells in a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Animal')
builder.insert_cell()
builder.write('Class')
builder.end_row()
builder.insert_cell()
builder.write('Dog')
builder.insert_cell()
builder.write('Mammal')
builder.end_table()
table.cell_spacing = 3
# Establezca la propiedad "AllowCellSpacing" a "true" para habilitar el espaciado entre celdas
# con una magnitud igual al valor de la propiedad "CellSpacing", en puntos.
# Establezca la propiedad "AllowCellSpacing" a "false" para desactivar el espaciado entre celdas
# y ignore el valor de la propiedad "CellSpacing".
table.allow_cell_spacing = allow_cell_spacing
doc.save(file_name=ARTIFACTS_DIR + 'Table.AllowCellSpacing.html')
# Ajustar la propiedad "CellSpacing" habilitará automáticamente el espaciado entre celdas.
table.cell_spacing = 5
self.assertTrue(table.allow_cell_spacing)
```

Shows how to create custom style settings for the table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Name')
builder.insert_cell()
builder.write('مرحبًا')
builder.end_row()
builder.insert_cell()
builder.insert_cell()
builder.end_table()
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
table_style.allow_break_across_pages = True
table_style.cell_spacing = 5
table_style.bottom_padding = 20
table_style.left_padding = 5
table_style.right_padding = 10
table_style.top_padding = 20
table_style.shading.background_pattern_color = aspose.pydrawing.Color.antique_white
table_style.borders.color = aspose.pydrawing.Color.blue
table_style.borders.line_style = aw.LineStyle.DOT_DASH
table_style.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
table.style = table_style
table.bidi = True
# Configurar las propiedades de estilo de una tabla puede afectar a las propiedades de la propia tabla.
self.assertTrue(table.bidi)
self.assertEqual(5, table.cell_spacing)
self.assertEqual('MyTableStyle1', table.style_name)
doc.save(file_name=ARTIFACTS_DIR + 'Table.TableStyleCreation.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

