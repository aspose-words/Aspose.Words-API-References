---
title: BorderCollection.vertical property
linktitle: vertical property
articleTitle: vertical property
second_title: Aspose.Words for Python
description: "BorderCollection.vertical property. Gets the vertical border that is used between cells."
type: docs
weight: 130
url: /tr/python-net/aspose.words/bordercollection/vertical/
---

## BorderCollection.vertical property

Gets the vertical border that is used between cells.


```python
@property
def vertical(self) -> aspose.words.Border:
    ...

```

### Examples

Shows how to apply settings to vertical borders to a table row's format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Kırmızı ve mavi iç kenarlıklarla bir tablo oluşturun.
table = builder.start_table()
i = 0
while i < 3:
    builder.insert_cell()
    builder.write(f'Row {i + 1}, Column 1')
    builder.insert_cell()
    builder.write(f'Row {i + 1}, Column 2')
    row = builder.end_row()
    borders = row.row_format.borders
    # Satırlar arasında görünecek kenarlıkların görünümünü ayarlayın.
    borders.horizontal.color = aspose.pydrawing.Color.red
    borders.horizontal.line_style = aw.LineStyle.DOT
    borders.horizontal.line_width = 2
    # Hücreler arasında görünecek kenarlıkların görünümünü ayarlayın.
    borders.vertical.color = aspose.pydrawing.Color.blue
    borders.vertical.line_style = aw.LineStyle.DOT
    borders.vertical.line_width = 2
    i += 1
# Satır biçimi ve bir hücrenin iç paragrafı farklı kenarlık ayarları kullanır.
border = table.first_row.first_cell.last_paragraph.paragraph_format.borders.vertical
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), border.color.to_argb())
self.assertEqual(0, border.line_width)
self.assertEqual(aw.LineStyle.NONE, border.line_style)
doc.save(file_name=ARTIFACTS_DIR + 'Border.VerticalBorders.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

