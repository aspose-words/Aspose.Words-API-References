---
title: ConditionalStyleCollection.last_column property
linktitle: last_column property
articleTitle: last_column property
second_title: Aspose.Words for Python
description: "ConditionalStyleCollection.last_column property. Gets the last column style."
type: docs
weight: 90
url: /es/python-net/aspose.words/conditionalstylecollection/last_column/
---

## ConditionalStyleCollection.last_column property

Gets the last column style.


```python
@property
def last_column(self) -> aspose.words.ConditionalStyle:
    ...

```

### Examples

Shows how to work with certain area styles of a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Cell 1')
builder.insert_cell()
builder.write('Cell 2')
builder.end_row()
builder.insert_cell()
builder.write('Cell 3')
builder.insert_cell()
builder.write('Cell 4')
builder.end_table()
# Cree un estilo de tabla personalizado.
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
# Los estilos condicionales son cambios de formato que afectan solo a algunas celdas de la tabla
# basados en un predicado, como que las celdas estén en la última fila.
# A continuación se presentan tres formas de acceder a los estilos condicionales de un estilo de tabla desde la colección "ConditionalStyles".
# 1 -  Por tipo de estilo:
table_style.conditional_styles.get_by_conditional_style_type(aw.ConditionalStyleType.FIRST_ROW).shading.background_pattern_color = drawing.Color.alice_blue
# 2 -  Por índice:
table_style.conditional_styles[0].borders.color = drawing.Color.black
table_style.conditional_styles[0].borders.line_style = aw.LineStyle.DOT_DASH
self.assertEqual(aw.ConditionalStyleType.FIRST_ROW, table_style.conditional_styles[0].type)
# 3 -  Como una propiedad:
table_style.conditional_styles.first_row.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
# Aplique relleno y formato de texto a los estilos condicionales.
table_style.conditional_styles.last_row.bottom_padding = 10
table_style.conditional_styles.last_row.left_padding = 10
table_style.conditional_styles.last_row.right_padding = 10
table_style.conditional_styles.last_row.top_padding = 10
table_style.conditional_styles.last_column.font.bold = True
# Enumere todas las condiciones de estilo posibles.
for style in table_style.conditional_styles:
    current_style = style
    if current_style is not None:
        print(current_style.type)
# Aplique el estilo personalizado, que contiene todos los estilos condicionales, a la tabla.
table.style = table_style
# Nuestro estilo aplica algunos estilos condicionales por defecto.
self.assertEqual(aw.tables.TableStyleOptions.FIRST_ROW | aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS, table.style_options)
# Necesitaremos habilitar todos los demás estilos nosotros mismos a través de la propiedad "StyleOptions".
table.style_options |= aw.tables.TableStyleOptions.LAST_ROW | aw.tables.TableStyleOptions.LAST_COLUMN
doc.save(file_name=ARTIFACTS_DIR + 'Table.ConditionalStyles.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyleCollection](../)

