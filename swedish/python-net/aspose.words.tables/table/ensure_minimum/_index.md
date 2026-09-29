---
title: Table.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Table.ensure_minimum method. If the table has no rows, creates and appends one [Row](../../row/)."
type: docs
weight: 420
url: /sv/python-net/aspose.words.tables/table/ensure_minimum/
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
# Tabeller innehåller rader, som innehåller celler, som kan innehålla stycken
# med typiska element som körningar, former och till och med andra tabeller.
# Vår nya tabell har inga av dessa noder, och vi kan inte lägga till innehåll i den förrän den har dem.
self.assertEqual(0, table.get_child_nodes(aw.NodeType.ANY, True).count)
# Att anropa "EnsureMinimum"-metoden på en tabell kommer att säkerställa att
# tabellen har minst en rad och en cell med ett tomt stycke.
table.ensure_minimum()
table.first_row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

