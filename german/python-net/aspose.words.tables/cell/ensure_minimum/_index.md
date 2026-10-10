---
title: Cell.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Cell.ensure_minimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 160
url: /de/python-net/aspose.words.tables/cell/ensure_minimum/
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
# Zellen können Absätze mit typischen Elementen wie Runs, Formen und sogar anderen Tabellen enthalten.
# Unsere neue Zelle hat keine Absätze, und wir können ihr keinen Inhalt wie Run- und Shape-Knoten hinzufügen, bis sie welche hat.
self.assertEqual(0, cell.get_child_nodes(aw.NodeType.ANY, True).count)
# Der Aufruf der Methode "EnsureMinimum" auf einer Zelle stellt sicher, dass
# die Zelle mindestens einen leeren Absatz hat, zu dem wir dann Inhalte hinzufügen können.
cell.ensure_minimum()
cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

