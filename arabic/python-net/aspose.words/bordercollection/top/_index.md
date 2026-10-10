---
title: BorderCollection.top property
linktitle: top property
articleTitle: top property
second_title: Aspose.Words for Python
description: "BorderCollection.top property. Gets the top border."
type: docs
weight: 120
url: /ar/python-net/aspose.words/bordercollection/top/
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
# ابدأ جدولًا واضبط اللون/السُمك الافتراضي لإطاراته.
table = builder.start_table()
table.set_borders(aw.LineStyle.SINGLE, 2, aspose.pydrawing.Color.black)
# أنشئ صفًا يحتوي على خليتين بألوان خلفية مختلفة.
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_sky_blue
builder.writeln('Row 1, Cell 1.')
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.orange
builder.writeln('Row 1, Cell 2.')
builder.end_row()
# أعد تعيين تنسيق الخلية لتعطيل ألوان الخلفية
# حدد سُمك إطار مخصص لجميع الخلايا الجديدة التي ينشئها المُنشئ،
# ثم أنشئ صفًا ثانيًا.
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

