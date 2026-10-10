---
title: Row.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Row.ensure_minimum method. If the [Row](../) has no cells, creates and appends one [Cell](../../cell/)."
type: docs
weight: 160
url: /ru/python-net/aspose.words.tables/row/ensure_minimum/
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
# Строки содержат ячейки, содержащие абзацы с типичными элементами, такими как пробеги, формы и даже другие таблицы.
# Наша новая строка не содержит ни одного из этих узлов, и мы не можем добавить содержимое, пока они не появятся.
self.assertEqual(0, row.get_child_nodes(aw.NodeType.ANY, True).count)
# Вызов метода "EnsureMinimum" у таблицы гарантирует, что
# В таблице есть как минимум одна ячейка с пустым абзацем.
row.ensure_minimum()
row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Row](../)

