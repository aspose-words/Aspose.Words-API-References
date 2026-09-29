---
title: BorderCollection.top property
linktitle: top property
articleTitle: top property
second_title: Aspose.Words for Python
description: "BorderCollection.top property. Gets the top border."
type: docs
weight: 120
url: /tr/python-net/aspose.words/bordercollection/top/
---

## BorderCollection.top property

Gets the top border.


```python
@property
def top(self) -> aspose.words.Border:
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

