---
title: ConditionalStyle.borders property
linktitle: borders property
articleTitle: borders property
second_title: Aspose.Words for Python
description: "ConditionalStyle.borders property. Gets the collection of default cell borders for the conditional style."
type: docs
weight: 10
url: /python-net/aspose.words/conditionalstyle/borders/
---

## ConditionalStyle.borders property

Gets the collection of default cell borders for the conditional style.


```python
@property
def borders(self) -> aspose.words.BorderCollection:
    ...

```

### Examples

Shows how to work with certain area styles of a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
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
# Create a custom table style.
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
# Conditional styles are formatting changes that affect only some of the table's cells
# based on a predicate, such as the cells being in the last row.
# Below are three ways of accessing a table style's conditional styles from the "conditional_styles" collection.
# 1 -  By style type:
table_style.conditional_styles[aw.ConditionalStyleType.FIRST_ROW].shading.background_pattern_color = aspose.pydrawing.Color.alice_blue
# 2 -  By index:
table_style.conditional_styles[0].borders.color = aspose.pydrawing.Color.black
table_style.conditional_styles[0].borders.line_style = aw.LineStyle.DOT_DASH
self.assertEqual(aw.ConditionalStyleType.FIRST_ROW, table_style.conditional_styles[0].type)
# 3 -  As a property:
table_style.conditional_styles.first_row.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
# Apply padding and text formatting to conditional styles.
table_style.conditional_styles.last_row.bottom_padding = 10
table_style.conditional_styles.last_row.left_padding = 10
table_style.conditional_styles.last_row.right_padding = 10
table_style.conditional_styles.last_row.top_padding = 10
table_style.conditional_styles.last_column.font.bold = True
# List all possible style conditions.
for conditional_style in table_style.conditional_styles:
    if conditional_style is not None:
        print(conditional_style.type)
# Apply the custom style, which contains all conditional styles, to the table.
table.style = table_style
# Our style applies some conditional styles by default.
self.assertEqual(aw.tables.TableStyleOptions.FIRST_ROW | aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS, table.style_options)
# We will need to enable all other styles ourselves via the "style_options" property.
table.style_options = table.style_options | aw.tables.TableStyleOptions.LAST_ROW | aw.tables.TableStyleOptions.LAST_COLUMN
doc.save(ARTIFACTS_DIR + 'Table.conditional_styles.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyle](../)

