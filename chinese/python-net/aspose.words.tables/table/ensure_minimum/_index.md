---
title: Table.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Table.ensure_minimum method. If the table has no rows, creates and appends one [Row](../../row/)."
type: docs
weight: 420
url: /zh/python-net/aspose.words.tables/table/ensure_minimum/
---

## ensure_minimum() {#default}

If the table has no rows, creates and appends one [Row](../../row/).



```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to ensure that a table node contains the nodes we need to add content.

```python
doc = aw.Document()
table = aw.tables.Table(doc)
doc.first_section.body.append_child(table)
# 表格包含行，行包含单元格，单元格可能包含段落
# 其中常见的元素包括文本运行、形状，甚至其他表格。
# 我们的新表格没有这些节点，且在出现这些节点之前我们无法向其添加内容。
self.assertEqual(0, table.get_child_nodes(aw.NodeType.ANY, True).count)
# 在表格上调用 "EnsureMinimum" 方法将确保
# 该表格至少有一行和一个带有空段落的单元格。
table.ensure_minimum()
table.first_row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

