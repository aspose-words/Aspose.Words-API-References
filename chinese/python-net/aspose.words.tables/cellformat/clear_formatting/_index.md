---
title: CellFormat.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "CellFormat.clear_formatting method. Resets to default cell formatting"
type: docs
weight: 160
url: /zh/python-net/aspose.words.tables/cellformat/clear_formatting/
---

## clear_formatting() {#default}

Resets to default cell formatting. Does not change the width of the cell.


```python
def clear_formatting(self):
    ...
```

### Examples

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
* class [CellFormat](../)

