---
title: CompositeNode.has_child_nodes property
linktitle: has_child_nodes property
articleTitle: has_child_nodes property
second_title: Aspose.Words for Python
description: "CompositeNode.has_child_nodes property. Returns ``True`` if this node has any child nodes."
type: docs
weight: 30
url: /zh/python-net/aspose.words/compositenode/has_child_nodes/
---

## CompositeNode.has_child_nodes property

Returns ``True`` if this node has any child nodes.



```python
@property
def has_child_nodes(self) -> bool:
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

* module [aspose.words](../../)
* class [CompositeNode](../)

