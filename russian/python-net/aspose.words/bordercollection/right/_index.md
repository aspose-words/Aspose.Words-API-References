---
title: BorderCollection.right property
linktitle: right property
articleTitle: right property
second_title: Aspose.Words for Python
description: "BorderCollection.right property. Gets the right border."
type: docs
weight: 100
url: /ru/python-net/aspose.words/bordercollection/right/
---

## BorderCollection.right property

Gets the right border.


```python
@property
def right(self) -> aspose.words.Border:
    ...

```

### Examples

Shows how to apply border and shading color while building a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте таблицу и задайте цвет/толщину по умолчанию для её границ.
table = builder.start_table()
table.set_borders(aw.LineStyle.SINGLE, 2, aspose.pydrawing.Color.black)
# Создайте строку с двумя ячейками с разными цветами фона.
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_sky_blue
builder.writeln('Row 1, Cell 1.')
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.orange
builder.writeln('Row 1, Cell 2.')
builder.end_row()
# Сбросьте форматирование ячейки, чтобы отключить цвета фона
# установите пользовательскую толщину границы для всех новых ячеек, создаваемых построителем,
# затем создайте вторую строку.
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

