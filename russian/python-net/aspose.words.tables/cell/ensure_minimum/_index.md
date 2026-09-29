---
title: Cell.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Cell.ensure_minimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 160
url: /ru/python-net/aspose.words.tables/cell/ensure_minimum/
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
# Ячейки могут содержать абзацы с типичными элементами, такими как run, shape и даже другие таблицы.
# Новая ячейка не содержит абзацев, и мы не можем добавить содержимое, такое как узлы run и shape, пока они не появятся.
self.assertEqual(0, cell.get_child_nodes(aw.NodeType.ANY, True).count)
# Вызов метода "EnsureMinimum" для ячейки гарантирует, что
# в ячейке будет как минимум один пустой абзац, к которому мы затем сможем добавить содержимое.
cell.ensure_minimum()
cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

