---
title: Cell.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Cell.ensure_minimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 160
url: /es/python-net/aspose.words.tables/cell/ensure_minimum/
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
# Las celdas pueden contener párrafos con elementos típicos como ejecuciones, formas y incluso otras tablas.
# Nuestra nueva celda no tiene ningún párrafo, y no podemos agregar contenido como nodos de ejecución y forma a ella hasta que los tenga.
self.assertEqual(0, cell.get_child_nodes(aw.NodeType.ANY, True).count)
# Llamar al método "EnsureMinimum" en una celda garantizará que
# la celda tenga al menos un párrafo vacío, al que luego podemos agregar contenido.
cell.ensure_minimum()
cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

