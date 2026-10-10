---
title: ConditionalStyleType enumeration
linktitle: ConditionalStyleType enumeration
articleTitle: ConditionalStyleType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ConditionalStyleType enumeration. Represents possible table areas to which conditional formatting may be defined in a table style."
type: docs
weight: 250
url: /ar/python-net/aspose.words/conditionalstyletype/
---

## ConditionalStyleType enumeration

Represents possible table areas to which conditional formatting may be defined in a table style.


### Members

| Name | Description |
| --- | --- |
| FIRST_ROW | Specifies formatting of the first row of a table. |
| FIRST_COLUMN | Specifies formatting of the first column of a table. |
| LAST_ROW | Specifies formatting of the last row of a table. |
| LAST_COLUMN | Specifies formatting of the last column of a table. |
| ODD_ROW_BANDING | Specifies formatting of odd-numbered row stripe. |
| ODD_COLUMN_BANDING | Specifies formatting of odd-numbered column stripe. |
| EVEN_ROW_BANDING | Specifies formatting of even-numbered row stripe. |
| EVEN_COLUMN_BANDING | Specifies formatting of even-numbered column stripe. |
| TOP_LEFT_CELL | Specifies formatting of the top left cell of a table. |
| TOP_RIGHT_CELL | Specifies formatting of the top right cell of a table. |
| BOTTOM_LEFT_CELL | Specifies formatting of the bottom left cell of a table. |
| BOTTOM_RIGHT_CELL | Specifies formatting of the bottom right cell of a table. |

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
# إنشاء نمط جدول مخصص.
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
# الأنماط الشرطية هي تغييرات تنسيق تؤثر فقط على بعض خلايا الجدول
# استنادًا إلى شرط، مثل كون الخلايا في الصف الأخير.
# فيما يلي ثلاث طرق للوصول إلى الأنماط الشرطية لنمط جدول من مجموعة "ConditionalStyles".
# 1 -  حسب نوع النمط:
table_style.conditional_styles.get_by_conditional_style_type(aw.ConditionalStyleType.FIRST_ROW).shading.background_pattern_color = drawing.Color.alice_blue
# 2 -  حسب الفهرس:
table_style.conditional_styles[0].borders.color = drawing.Color.black
table_style.conditional_styles[0].borders.line_style = aw.LineStyle.DOT_DASH
self.assertEqual(aw.ConditionalStyleType.FIRST_ROW, table_style.conditional_styles[0].type)
# 3 -  كخاصية:
table_style.conditional_styles.first_row.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
# طبق الحشو وتنسيق النص على الأنماط الشرطية.
table_style.conditional_styles.last_row.bottom_padding = 10
table_style.conditional_styles.last_row.left_padding = 10
table_style.conditional_styles.last_row.right_padding = 10
table_style.conditional_styles.last_row.top_padding = 10
table_style.conditional_styles.last_column.font.bold = True
# قائمة بجميع شروط الأنماط الممكنة.
for style in table_style.conditional_styles:
    current_style = style
    if current_style is not None:
        print(current_style.type)
# طبق النمط المخصص، الذي يحتوي على جميع الأنماط الشرطية، على الجدول.
table.style = table_style
# نمطنا يطبق بعض الأنماط الشرطية بشكل افتراضي.
self.assertEqual(aw.tables.TableStyleOptions.FIRST_ROW | aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS, table.style_options)
# سنحتاج إلى تمكين جميع الأنماط الأخرى بأنفسنا عبر خاصية "StyleOptions".
table.style_options |= aw.tables.TableStyleOptions.LAST_ROW | aw.tables.TableStyleOptions.LAST_COLUMN
doc.save(file_name=ARTIFACTS_DIR + 'Table.ConditionalStyles.docx')
```

### See Also

* module [aspose.words](../)

