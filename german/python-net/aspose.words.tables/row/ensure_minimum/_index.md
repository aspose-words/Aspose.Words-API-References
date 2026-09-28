---
title: Row.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Row.ensure_minimum method. If the [Row](../) has no cells, creates and appends one [Cell](../../cell/)."
type: docs
weight: 160
url: /de/python-net/aspose.words.tables/row/ensure_minimum/
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
# Zeilen enthalten Zellen, die Absätze mit typischen Elementen wie Textläufen, Formen und sogar anderen Tabellen enthalten.
# Unsere neue Zeile enthält keine dieser Knoten, und wir können ihr keinen Inhalt hinzufügen, bis sie das tut.
self.assertEqual(0, row.get_child_nodes(aw.NodeType.ANY, True).count)
# Der Aufruf der "EnsureMinimum"-Methode auf einer Tabelle stellt sicher, dass
# Die Tabelle hat mindestens eine Zelle mit einem leeren Absatz.
row.ensure_minimum()
row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Row](../)

