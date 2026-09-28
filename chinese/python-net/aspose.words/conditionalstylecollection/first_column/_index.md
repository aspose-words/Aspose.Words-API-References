---
title: ConditionalStyleCollection.first_column property
linktitle: first_column property
articleTitle: first_column property
second_title: Aspose.Words for Python
description: "ConditionalStyleCollection.first_column property. Gets the first column style."
type: docs
weight: 70
url: /zh/python-net/aspose.words/conditionalstylecollection/first_column/
---

## ConditionalStyleCollection.first_column property

Gets the first column style.


```python
@property
def first_column(self) -> aspose.words.ConditionalStyle:
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
# 创建自定义表格样式。
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
# 条件样式是仅影响表格部分单元格的格式更改
# 基于谓词，例如单元格位于最后一行时。
# 下面是从 "ConditionalStyles" 集合中访问表格样式的条件样式的三种方式。
# 1 -  按样式类型：
table_style.conditional_styles.get_by_conditional_style_type(aw.ConditionalStyleType.FIRST_ROW).shading.background_pattern_color = drawing.Color.alice_blue
# 2 -  按索引：
table_style.conditional_styles[0].borders.color = drawing.Color.black
table_style.conditional_styles[0].borders.line_style = aw.LineStyle.DOT_DASH
self.assertEqual(aw.ConditionalStyleType.FIRST_ROW, table_style.conditional_styles[0].type)
# 3 -  作为属性：
table_style.conditional_styles.first_row.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
# 对条件样式应用填充和文本格式。
table_style.conditional_styles.last_row.bottom_padding = 10
table_style.conditional_styles.last_row.left_padding = 10
table_style.conditional_styles.last_row.right_padding = 10
table_style.conditional_styles.last_row.top_padding = 10
table_style.conditional_styles.last_column.font.bold = True
# 列出所有可能的样式条件。
for style in table_style.conditional_styles:
    current_style = style
    if current_style is not None:
        print(current_style.type)
# 将包含所有条件样式的自定义样式应用于表格。
table.style = table_style
# 我们的样式默认应用了一些条件样式。
self.assertEqual(aw.tables.TableStyleOptions.FIRST_ROW | aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS, table.style_options)
# 我们需要通过 "StyleOptions" 属性自行启用所有其他样式。
table.style_options |= aw.tables.TableStyleOptions.LAST_ROW | aw.tables.TableStyleOptions.LAST_COLUMN
doc.save(file_name=ARTIFACTS_DIR + 'Table.ConditionalStyles.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyleCollection](../)

