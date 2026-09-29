---
title: ConditionalStyleCollection.even_row_banding property
linktitle: even_row_banding property
articleTitle: even_row_banding property
second_title: Aspose.Words for Python
description: "ConditionalStyleCollection.even_row_banding property. Gets the even row banding style."
type: docs
weight: 60
url: /ru/python-net/aspose.words/conditionalstylecollection/even_row_banding/
---

## ConditionalStyleCollection.even_row_banding property

Gets the even row banding style.


```python
@property
def even_row_banding(self) -> aspose.words.ConditionalStyle:
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
# Создайте пользовательский стиль таблицы.
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
# Условные стили — это изменения форматирования, которые влияют только на некоторые ячейки таблицы
# на основе предиката, например, ячейки, находящиеся в последней строке.
# Ниже представлены три способа доступа к условным стилям стиля таблицы из коллекции "ConditionalStyles".
# 1 -  По типу стиля:
table_style.conditional_styles.get_by_conditional_style_type(aw.ConditionalStyleType.FIRST_ROW).shading.background_pattern_color = drawing.Color.alice_blue
# 2 -  По индексу:
table_style.conditional_styles[0].borders.color = drawing.Color.black
table_style.conditional_styles[0].borders.line_style = aw.LineStyle.DOT_DASH
self.assertEqual(aw.ConditionalStyleType.FIRST_ROW, table_style.conditional_styles[0].type)
# 3 -  Как свойство:
table_style.conditional_styles.first_row.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
# Примените отступы и форматирование текста к условным стилям.
table_style.conditional_styles.last_row.bottom_padding = 10
table_style.conditional_styles.last_row.left_padding = 10
table_style.conditional_styles.last_row.right_padding = 10
table_style.conditional_styles.last_row.top_padding = 10
table_style.conditional_styles.last_column.font.bold = True
# Выведите список всех возможных условий стилей.
for style in table_style.conditional_styles:
    current_style = style
    if current_style is not None:
        print(current_style.type)
# Примените пользовательский стиль, содержащий все условные стили, к таблице.
table.style = table_style
# Наш стиль по умолчанию применяет некоторые условные стили.
self.assertEqual(aw.tables.TableStyleOptions.FIRST_ROW | aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS, table.style_options)
# Нам придётся включить все остальные стили самостоятельно через свойство "StyleOptions".
table.style_options |= aw.tables.TableStyleOptions.LAST_ROW | aw.tables.TableStyleOptions.LAST_COLUMN
doc.save(file_name=ARTIFACTS_DIR + 'Table.ConditionalStyles.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyleCollection](../)

