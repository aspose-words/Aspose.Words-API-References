---
title: BorderCollection.bottom property
linktitle: bottom property
articleTitle: bottom property
second_title: Aspose.Words for Python
description: "BorderCollection.bottom property. Gets the bottom border."
type: docs
weight: 20
url: /tr/python-net/aspose.words/bordercollection/bottom/
---

## BorderCollection.bottom property

Gets the bottom border.


```python
@property
def bottom(self) -> aspose.words.Border:
    ...

```

### Examples

Shows how to apply border and shading color while building a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir tablo başlatın ve kenarları için varsayılan renk/kalınlığı ayarlayın.
table = builder.start_table()
table.set_borders(aw.LineStyle.SINGLE, 2, aspose.pydrawing.Color.black)
# Farklı arka plan renklerine sahip iki hücreli bir satır oluşturun.
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_sky_blue
builder.writeln('Row 1, Cell 1.')
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.orange
builder.writeln('Row 1, Cell 2.')
builder.end_row()
# Hücre biçimlendirmesini sıfırlayarak arka plan renklerini devre dışı bırakın
# Derleyici tarafından oluşturulan tüm yeni hücreler için özel bir kenar kalınlığı ayarlayın,
# sonra ikinci bir satır oluşturun.
builder.cell_format.clear_formatting()
builder.cell_format.borders.left.line_width = 4
builder.cell_format.borders.right.line_width = 4
builder.cell_format.borders.top.line_width = 4
builder.cell_format.borders.bottom.line_width = 4
builder.insert_cell()
builder.writeln('Row 2, Cell 1.')
builder.insert_cell()
builder.writeln('Row 2, Cell 2.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.TableBordersAndShading.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

