---
title: Table.allow_auto_fit property
linktitle: allow_auto_fit property
articleTitle: allow_auto_fit property
second_title: Aspose.Words for Python
description: "Table.allow_auto_fit property. Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents."
type: docs
weight: 50
url: /zh/python-net/aspose.words.tables/table/allow_auto_fit/
---

## Table.allow_auto_fit property

Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.


```python
@property
def allow_auto_fit(self) -> bool:
    ...

@allow_auto_fit.setter
def allow_auto_fit(self, value: bool):
    ...

```

### Remarks

The default value is ``True``.




### Examples

Shows how to enable/disable automatic table cell resizing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_points(100)
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.AUTO
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
builder.end_row()
builder.end_table()
# 将 "AllowAutoFit" 属性设置为 "false"，以使表格保持尺寸
# 保持所有行和单元格的尺寸，并在内容过大而无法容纳时进行截断。
# 将 "AllowAutoFit" 属性设置为 "true"，以允许表格更改其单元格的宽度和高度
# 以适应其内容。
table.allow_auto_fit = allow_auto_fit
doc.save(file_name=ARTIFACTS_DIR + 'Table.AllowAutoFitOnTable.html')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)
* method [Table.auto_fit()](../auto_fit/#autofitbehavior)

