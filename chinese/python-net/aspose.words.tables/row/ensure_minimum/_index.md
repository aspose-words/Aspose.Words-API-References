---
title: Row.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Row.ensure_minimum method. If the [Row](../) has no cells, creates and appends one [Cell](../../cell/)."
type: docs
weight: 160
url: /zh/python-net/aspose.words.tables/row/ensure_minimum/
---

## ensure_minimum() {#default}

If the [Row](../) has no cells, creates and appends one [Cell](../../cell/).



```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to ensure a row node contains the nodes we need to begin adding content to it.

```python
doc = aw.Document()
table = aw.tables.Table(doc)
doc.first_section.body.append_child(table)
row = aw.tables.Row(doc)
table.append_child(row)
# 行包含单元格，单元格中包含带有常见元素（如文本段、形状，甚至其他表格）的段落。
# 我们的新行没有这些节点，且在它拥有这些节点之前我们无法向其添加内容。
self.assertEqual(0, row.get_child_nodes(aw.NodeType.ANY, True).count)
# 在表格上调用 "EnsureMinimum" 方法将确保
# 表格至少有一个单元格包含空段落。
row.ensure_minimum()
row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Row](../)

