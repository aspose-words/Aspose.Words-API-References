---
title: ConditionalStyleCollection class
linktitle: ConditionalStyleCollection class
articleTitle: ConditionalStyleCollection class
second_title: Aspose.Words for Python
description: "aspose.words.ConditionalStyleCollection class. Represents a collection of [ConditionalStyle](../conditionalstyle/) objects"
type: docs
weight: 240
url: /fr/python-net/aspose.words/conditionalstylecollection/
---

## ConditionalStyleCollection class

Represents a collection of [ConditionalStyle](../conditionalstyle/) objects.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/python-net/working-with-tables/) documentation article.




### Remarks

It is not possible to add or remove items from this collection. It contains permanent set of items: one item for
each value of the [ConditionalStyleType](../conditionalstyletype/) enumeration type.



### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [ConditionalStyle](../conditionalstyle/) object by index. |

### Properties

| Name | Description |
| --- | --- |
| [bottom_left_cell](./bottom_left_cell/) | Gets the bottom left cell style. |
| [bottom_right_cell](./bottom_right_cell/) | Gets the bottom right cell style. |
| [count](./count/) | Gets the number of conditional styles in the collection. |
| [even_column_banding](./even_column_banding/) | Gets the even column banding style. |
| [even_row_banding](./even_row_banding/) | Gets the even row banding style. |
| [first_column](./first_column/) | Gets the first column style. |
| [first_row](./first_row/) | Gets the first row style. |
| [last_column](./last_column/) | Gets the last column style. |
| [last_row](./last_row/) | Gets the last row style. |
| [odd_column_banding](./odd_column_banding/) | Gets the odd column banding style. |
| [odd_row_banding](./odd_row_banding/) | Gets the odd row banding style. |
| [top_left_cell](./top_left_cell/) | Gets the top left cell style. |
| [top_right_cell](./top_right_cell/) | Gets the top right cell style. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Clears all conditional styles of the table style. |

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
# Créez un style de tableau personnalisé.
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
# Les styles conditionnels sont des modifications de mise en forme qui n'affectent que certaines cellules du tableau
# basées sur un prédicat, comme les cellules se trouvant dans la dernière ligne.
# Voici trois façons d'accéder aux styles conditionnels d'un style de tableau depuis la collection "ConditionalStyles".
# 1 -  Par type de style :
table_style.conditional_styles.get_by_conditional_style_type(aw.ConditionalStyleType.FIRST_ROW).shading.background_pattern_color = drawing.Color.alice_blue
# 2 -  Par index :
table_style.conditional_styles[0].borders.color = drawing.Color.black
table_style.conditional_styles[0].borders.line_style = aw.LineStyle.DOT_DASH
self.assertEqual(aw.ConditionalStyleType.FIRST_ROW, table_style.conditional_styles[0].type)
# 3 -  En tant que propriété :
table_style.conditional_styles.first_row.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
# Appliquez le remplissage et la mise en forme du texte aux styles conditionnels.
table_style.conditional_styles.last_row.bottom_padding = 10
table_style.conditional_styles.last_row.left_padding = 10
table_style.conditional_styles.last_row.right_padding = 10
table_style.conditional_styles.last_row.top_padding = 10
table_style.conditional_styles.last_column.font.bold = True
# Listez toutes les conditions de style possibles.
for style in table_style.conditional_styles:
    current_style = style
    if current_style is not None:
        print(current_style.type)
# Appliquez le style personnalisé, qui contient tous les styles conditionnels, au tableau.
table.style = table_style
# Notre style applique certains styles conditionnels par défaut.
self.assertEqual(aw.tables.TableStyleOptions.FIRST_ROW | aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS, table.style_options)
# Nous devrons activer tous les autres styles nous-mêmes via la propriété "StyleOptions".
table.style_options |= aw.tables.TableStyleOptions.LAST_ROW | aw.tables.TableStyleOptions.LAST_COLUMN
doc.save(file_name=ARTIFACTS_DIR + 'Table.ConditionalStyles.docx')
```

### See Also

* module [aspose.words](../)

