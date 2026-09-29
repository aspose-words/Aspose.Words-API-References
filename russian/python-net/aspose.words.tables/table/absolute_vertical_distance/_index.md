---
title: Table.absolute_vertical_distance property
linktitle: absolute_vertical_distance property
articleTitle: absolute_vertical_distance property
second_title: Aspose.Words for Python
description: "Table.absolute_vertical_distance property. Gets or sets absolute vertical floating table position specified by the table properties, in points"
type: docs
weight: 30
url: /ru/python-net/aspose.words.tables/table/absolute_vertical_distance/
---

## Table.absolute_vertical_distance property

Gets or sets absolute vertical floating table position specified by the table properties, in points.
Default value is 0.


```python
@property
def absolute_vertical_distance(self) -> float:
    ...

@absolute_vertical_distance.setter
def absolute_vertical_distance(self, value: float):
    ...

```

### Examples

Shows how set the location of floating tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Table 1, cell 1')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
# Установите расположение таблицы в определённое место на странице, например, в данном случае — в правый нижний угол.
table.relative_vertical_alignment = aw.drawing.VerticalAlignment.BOTTOM
table.relative_horizontal_alignment = aw.drawing.HorizontalAlignment.RIGHT
table = builder.start_table()
builder.insert_cell()
builder.write('Table 2, cell 1')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
# Мы также можем задать горизонтальное и вертикальное смещение в пунктах от положения абзаца, где мы вставили таблицу.
table.absolute_vertical_distance = 50
table.absolute_horizontal_distance = 100
doc.save(file_name=ARTIFACTS_DIR + 'Table.ChangeFloatingTableProperties.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

