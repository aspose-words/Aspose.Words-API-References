---
title: PreferredWidth.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for Python
description: "PreferredWidth.equals method. Determines whether the specified [PreferredWidth](../) is equal in value to the current [PreferredWidth](../)."
type: docs
weight: 40
url: /zh/python-net/aspose.words.tables/preferredwidth/equals/
---

## equals(other) {#preferredwidth}

Determines whether the specified [PreferredWidth](../) is equal in value to the current [PreferredWidth](../).



```python
def equals(self, other: aspose.words.tables.PreferredWidth):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| other | [PreferredWidth](../) |  |

### Examples

Shows how to set a preferred width for table cells.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
# 对表格单元格应用 "PreferredWidth" 类有两种方式。
# 1 - 基于点设置绝对首选宽度：
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_points(40)
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_yellow
builder.writeln(f'Cell with a width of {builder.cell_format.preferred_width}.')
# 2 - 基于表格宽度的百分比设置相对首选宽度：
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_percent(20)
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_blue
builder.writeln(f'Cell with a width of {builder.cell_format.preferred_width}.')
builder.insert_cell()
# 未指定首选宽度的单元格将占用剩余的可用空间。
builder.cell_format.preferred_width = aw.tables.PreferredWidth.AUTO
# 每次对 \"PreferredWidth\" 属性的配置都会创建一个新对象。
self.assertNotEqual(hash(table.first_row.cells[1].cell_format.preferred_width), hash(builder.cell_format.preferred_width))
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_green
builder.writeln('Automatically sized cell.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertCellsWithPreferredWidths.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [PreferredWidth](../)

