---
title: TableStyle.row_stripe property
linktitle: row_stripe property
articleTitle: row_stripe property
second_title: Aspose.Words for Python
description: "TableStyle.row_stripe property. Gets or sets a number of rows to include in the banding when the style specifies odd/even row banding."
type: docs
weight: 120
url: /python-net/aspose.words/tablestyle/row_stripe/
---

## TableStyle.row_stripe property

Gets or sets a number of rows to include in the banding when the style specifies odd/even row banding.


```python
@property
def row_stripe(self) -> int:
    ...

@row_stripe.setter
def row_stripe(self, value: int):
    ...

```

### Examples

Shows how to create conditional table styles that alternate between rows.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# We can configure a conditional style of a table to apply a different color to the row/column,
# based on whether the row/column is even or odd, creating an alternating color pattern.
# We can also apply a number n to the row/column banding,
# meaning that the color alternates after every n rows/columns instead of one.
# Create a table where single columns and rows will band the columns will banded in threes.
table = builder.start_table()
for i in range(15):
    for j in range(4):
        builder.insert_cell()
        builder.writeln(f"{('Even' if j % 2 == 0 else 'Odd')} column.")
        builder.write(f"Row banding {('start' if i % 3 == 0 else 'continuation')}.")
    builder.end_row()
builder.end_table()
# Apply a line style to all the borders of the table.
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
table_style.borders.color = aspose.pydrawing.Color.black
table_style.borders.line_style = aw.LineStyle.DOUBLE
# Set the two colors, which will alternate over every 3 rows.
table_style.row_stripe = 3
table_style.conditional_styles[aw.ConditionalStyleType.ODD_ROW_BANDING].shading.background_pattern_color = aspose.pydrawing.Color.light_blue
table_style.conditional_styles[aw.ConditionalStyleType.EVEN_ROW_BANDING].shading.background_pattern_color = aspose.pydrawing.Color.light_cyan
# Set a color to apply to every even column, which will override any custom row coloring.
table_style.column_stripe = 1
table_style.conditional_styles[aw.ConditionalStyleType.EVEN_COLUMN_BANDING].shading.background_pattern_color = aspose.pydrawing.Color.light_salmon
table.style = table_style
# The "style_options" property enables row banding by default.
self.assertEqual(aw.tables.TableStyleOptions.FIRST_ROW | aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS, table.style_options)
# Use the "style_options" property also to enable column banding.
table.style_options = table.style_options | aw.tables.TableStyleOptions.COLUMN_BANDS
doc.save(ARTIFACTS_DIR + 'Table.alternating_row_styles.docx')
```

### See Also

* module [aspose.words](../../)
* class [TableStyle](../)

