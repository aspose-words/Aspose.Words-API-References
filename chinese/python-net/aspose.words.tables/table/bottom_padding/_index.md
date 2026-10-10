---
title: Table.bottom_padding property
linktitle: bottom_padding property
articleTitle: bottom_padding property
second_title: Aspose.Words for Python
description: "Table.bottom_padding property. Gets or sets the amount of space (in points) to add below the contents of cells."
type: docs
weight: 90
url: /zh/python-net/aspose.words.tables/table/bottom_padding/
---

## Table.bottom_padding property

Gets or sets the amount of space (in points) to add below the contents of cells.


```python
@property
def bottom_padding(self) -> float:
    ...

@bottom_padding.setter
def bottom_padding(self, value: float):
    ...

```

### Examples

Shows how to configure content padding in a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
builder.insert_cell()
builder.write('Row 1, cell 2.')
builder.end_table()
# 对于表格中的每个单元格，设置其内容与各边框之间的距离。
# 此表格将通过换行文本来保持最小的内边距距离。
table.left_padding = 30
table.right_padding = 60
table.top_padding = 10
table.bottom_padding = 90
table.preferred_width = aw.tables.PreferredWidth.from_points(250)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetRowFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

