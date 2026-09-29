---
title: Table.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Table.ensure_minimum method. If the table has no rows, creates and appends one [Row](../../row/)."
type: docs
weight: 420
url: /it/python-net/aspose.words.tables/table/ensure_minimum/
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
# Le tabelle contengono righe, che contengono celle, che possono contenere paragrafi
# con elementi tipici come run, forme e persino altre tabelle.
# La nostra nuova tabella non ha nessuno di questi nodi, e non possiamo aggiungere contenuti finché non li ha.
self.assertEqual(0, table.get_child_nodes(aw.NodeType.ANY, True).count)
# Chiamare il metodo "EnsureMinimum" su una tabella garantirà che
# la tabella ha almeno una riga e una cella con un paragrafo vuoto.
table.ensure_minimum()
table.first_row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

