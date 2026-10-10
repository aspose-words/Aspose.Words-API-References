---
title: ConditionalStyle.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "ConditionalStyle.type property. Gets table area to which this conditional style relates."
type: docs
weight: 90
url: /sv/python-net/aspose.words/conditionalstyle/type/
---

## ConditionalStyle.type property

Gets table area to which this conditional style relates.


```python
@property
def type(self) -> aspose.words.ConditionalStyleType:
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
# Skapa en anpassad tabellstil.
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
# Villkorliga stilar är formateringsändringar som endast påverkar vissa av tabellens celler
# baserat på ett villkor, såsom att cellerna är i den sista raden.
# Nedan följer tre sätt att komma åt en tabellstils villkorliga stilar från samlingen "ConditionalStyles".
# 1 -  Efter stiltyp:
table_style.conditional_styles.get_by_conditional_style_type(aw.ConditionalStyleType.FIRST_ROW).shading.background_pattern_color = drawing.Color.alice_blue
# 2 -  Efter index:
table_style.conditional_styles[0].borders.color = drawing.Color.black
table_style.conditional_styles[0].borders.line_style = aw.LineStyle.DOT_DASH
self.assertEqual(aw.ConditionalStyleType.FIRST_ROW, table_style.conditional_styles[0].type)
# 3 -  Som en egenskap:
table_style.conditional_styles.first_row.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
# Applicera utfyllnad och textformatering på villkorliga stilar.
table_style.conditional_styles.last_row.bottom_padding = 10
table_style.conditional_styles.last_row.left_padding = 10
table_style.conditional_styles.last_row.right_padding = 10
table_style.conditional_styles.last_row.top_padding = 10
table_style.conditional_styles.last_column.font.bold = True
# Lista alla möjliga stilvillkor.
for style in table_style.conditional_styles:
    current_style = style
    if current_style is not None:
        print(current_style.type)
# Applicera den anpassade stilen, som innehåller alla villkorliga stilar, på tabellen.
table.style = table_style
# Vår stil tillämpar vissa villkorliga stilar som standard.
self.assertEqual(aw.tables.TableStyleOptions.FIRST_ROW | aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS, table.style_options)
# Vi kommer behöva aktivera alla andra stilar själva via egenskapen "StyleOptions".
table.style_options |= aw.tables.TableStyleOptions.LAST_ROW | aw.tables.TableStyleOptions.LAST_COLUMN
doc.save(file_name=ARTIFACTS_DIR + 'Table.ConditionalStyles.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyle](../)

