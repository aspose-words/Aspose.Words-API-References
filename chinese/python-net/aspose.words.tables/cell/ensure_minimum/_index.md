---
title: Cell.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Cell.ensure_minimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 160
url: /zh/python-net/aspose.words.tables/cell/ensure_minimum/
---

## ensure_minimum() {#default}

If the last child is not a paragraph, creates and appends one empty paragraph.


```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to ensure a cell node contains the nodes we need to begin adding content to it.

```python
doc = aw.Document()
table = aw.tables.Table(doc)
doc.first_section.body.append_child(table)
row = aw.tables.Row(doc)
table.append_child(row)
cell = aw.tables.Cell(doc)
row.append_child(cell)
# 单元格可以包含带有常见元素的段落，例如运行、形状，甚至其他表格。
# 我们的新单元格没有任何段落，在它拥有段落之前我们无法向其添加诸如运行和形状节点之类的内容。
self.assertEqual(0, cell.get_child_nodes(aw.NodeType.ANY, True).count)
# 在单元格上调用 "EnsureMinimum" 方法将确保
# 该单元格至少有一个空段落，随后我们可以向其添加内容。
cell.ensure_minimum()
cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

