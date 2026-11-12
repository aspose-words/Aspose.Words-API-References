---
title: ConditionalStyleCollection.odd_row_banding property
linktitle: odd_row_banding property
articleTitle: odd_row_banding property
second_title: Aspose.Words for Python
description: "ConditionalStyleCollection.odd_row_banding property. Gets the odd row banding style."
type: docs
weight: 120
url: /tr/python-net/aspose.words/conditionalstylecollection/odd_row_banding/
---

## ConditionalStyleCollection.odd_row_banding property

Gets the odd row banding style.


```python
@property
def odd_row_banding(self) -> aspose.words.ConditionalStyle:
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
# Özel bir tablo stili oluşturun.
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
# Koşullu stiller, yalnızca tablonun bazı hücrelerini etkileyen biçimlendirme değişiklikleridir
# bir koşula dayanarak, örneğin hücrelerin son satırda olması gibi.
# Aşağıda, bir tablo stilinin koşullu stillerine "ConditionalStyles" koleksiyonundan erişmenin üç yolu verilmiştir.
# 1 -  Stil türüne göre:
table_style.conditional_styles.get_by_conditional_style_type(aw.ConditionalStyleType.FIRST_ROW).shading.background_pattern_color = drawing.Color.alice_blue
# 2 -  İndexe göre:
table_style.conditional_styles[0].borders.color = drawing.Color.black
table_style.conditional_styles[0].borders.line_style = aw.LineStyle.DOT_DASH
self.assertEqual(aw.ConditionalStyleType.FIRST_ROW, table_style.conditional_styles[0].type)
# 3 -  Bir özellik olarak:
table_style.conditional_styles.first_row.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
# Koşullu stillere dolgu ve metin biçimlendirmesi uygulayın.
table_style.conditional_styles.last_row.bottom_padding = 10
table_style.conditional_styles.last_row.left_padding = 10
table_style.conditional_styles.last_row.right_padding = 10
table_style.conditional_styles.last_row.top_padding = 10
table_style.conditional_styles.last_column.font.bold = True
# Tüm olası stil koşullarını listeleyin.
for style in table_style.conditional_styles:
    current_style = style
    if current_style is not None:
        print(current_style.type)
# Tüm koşullu stilleri içeren özel stili tabloya uygulayın.
table.style = table_style
# Stilimiz varsayılan olarak bazı koşullu stilleri uygular.
self.assertEqual(aw.tables.TableStyleOptions.FIRST_ROW | aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS, table.style_options)
# "StyleOptions" özelliği aracılığıyla diğer tüm stilleri kendimiz etkinleştirmemiz gerekecek.
table.style_options |= aw.tables.TableStyleOptions.LAST_ROW | aw.tables.TableStyleOptions.LAST_COLUMN
doc.save(file_name=ARTIFACTS_DIR + 'Table.ConditionalStyles.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyleCollection](../)

