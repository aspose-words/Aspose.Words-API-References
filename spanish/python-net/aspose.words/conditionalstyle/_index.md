---
title: ConditionalStyle class
linktitle: ConditionalStyle class
articleTitle: ConditionalStyle class
second_title: Aspose.Words for Python
description: "aspose.words.ConditionalStyle class. Represents special formatting applied to some area of a table with assigned table style"
type: docs
weight: 230
url: /es/python-net/aspose.words/conditionalstyle/
---

## ConditionalStyle class

Represents special formatting applied to some area of a table with assigned table style.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/python-net/working-with-tables/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [borders](./borders/) | Gets the collection of default cell borders for the conditional style. |
| [bottom_padding](./bottom_padding/) | Gets or sets the amount of space (in points) to add below the contents of table cells. |
| [font](./font/) | Gets the character formatting of the conditional style. |
| [left_padding](./left_padding/) | Gets or sets the amount of space (in points) to add to the left of the contents of table cells. |
| [paragraph_format](./paragraph_format/) | Gets the paragraph formatting of the conditional style. |
| [right_padding](./right_padding/) | Gets or sets the amount of space (in points) to add to the right of the contents of table cells. |
| [shading](./shading/) | Gets a [Shading](../shading/) object that refers to the shading formatting for this conditional style. |
| [top_padding](./top_padding/) | Gets or sets the amount of space (in points) to add above the contents of table cells. |
| [type](./type/) | Gets table area to which this conditional style relates. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Clears formatting of this conditional style. |

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

* module [aspose.words](../)

