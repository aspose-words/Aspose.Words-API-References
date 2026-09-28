---
title: Table.rows property
linktitle: rows property
articleTitle: rows property
second_title: Aspose.Words for Python
description: "Table.rows property. Provides typed access to the rows of the table."
type: docs
weight: 260
url: /zh/python-net/aspose.words.tables/table/rows/
---

## Table.rows property

Provides typed access to the rows of the table.


```python
@property
def rows(self) -> aspose.words.tables.RowCollection:
    ...

```

### Examples

Shows how to iterate through all tables in the document and print the contents of each cell.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
tables = doc.first_section.body.tables
self.assertEqual(2, len(list(tables)))
i = 0
while i < tables.count:
    print(f'Start of Table {i}')
    rows = tables[i].rows
    # 我们可以在行集合上使用 "ToArray" 方法将其克隆为数组。
    assert rows == rows.to_array()
    self.assertNotEqual(rows, list(rows))
    j = 0
    while j < rows.count:
        print(f'\tStart of Row {j}')
        cells = rows[j].cells
        # 我们可以在单元格集合上使用 "ToArray" 方法将其克隆为数组。
        assert cells == cells.to_array()
        self.assertNotEqual(cells, list(cells))
        k = 0
        while k < cells.count:
            cell_text = cells[k].to_string(save_format=aw.SaveFormat.TEXT).strip()
            print(f'\t\tContents of Cell:{k} = "{cell_text}"')
            k += 1
        print(f'\tEnd of Row {j}')
        j += 1
    print(f'End of Table {i}\n')
    i += 1
```

Shows how to combine the rows from two tables into one.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
# 以下是从文档中获取表格的两种方法。
# 1 - 从 Body 节点的 \"Tables\" 集合中获取：
first_table = doc.first_section.body.tables[0]
# 2 - 使用 \"GetChild\" 方法：
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()
# 将当前表格的所有行追加到下一个表格中。
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)
# 删除空的表格容器。
second_table.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Table.CombineTables.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

