---
title: Table.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Table.ensure_minimum method. If the table has no rows, creates and appends one [Row](../../row/)."
type: docs
weight: 420
url: /ru/python-net/aspose.words.tables/table/ensure_minimum/
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
# Таблицы содержат строки, которые содержат ячейки, которые могут содержать абзацы
# с типичными элементами, такими как текстовые фрагменты, фигуры и даже другие таблицы.
# В нашей новой таблице нет этих узлов, и мы не можем добавить содержимое, пока они не появятся.
self.assertEqual(0, table.get_child_nodes(aw.NodeType.ANY, True).count)
# Вызов метода "EnsureMinimum" у таблицы гарантирует, что
# Таблица имеет как минимум одну строку и одну ячейку с пустым абзацем.
table.ensure_minimum()
table.first_row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

