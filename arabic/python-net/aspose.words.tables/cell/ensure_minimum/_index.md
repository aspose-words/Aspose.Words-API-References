---
title: Cell.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Cell.ensure_minimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 160
url: /ar/python-net/aspose.words.tables/cell/ensure_minimum/
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
# قد تحتوي الخلايا على فقرات تحتوي على عناصر نموذجية مثل التشغيلات، الأشكال، وحتى جداول أخرى.
# الخلية الجديدة لدينا لا تحتوي على أي فقرات، ولا يمكننا إضافة محتويات مثل عقد التشغيل والشكل إليها حتى تحتويها.
self.assertEqual(0, cell.get_child_nodes(aw.NodeType.ANY, True).count)
# استدعاء طريقة "EnsureMinimum" على خلية سيضمن أن
# الخلية تحتوي على فقرة فارغة واحدة على الأقل، والتي يمكننا بعد ذلك إضافة محتويات إليها.
cell.ensure_minimum()
cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

