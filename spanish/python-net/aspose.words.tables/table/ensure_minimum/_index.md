---
title: Table.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Table.ensure_minimum method. If the table has no rows, creates and appends one [Row](../../row/)."
type: docs
weight: 420
url: /es/python-net/aspose.words.tables/table/ensure_minimum/
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
# Las tablas contienen filas, que contienen celdas, que pueden contener párrafos
# con elementos típicos como ejecuciones, formas e incluso otras tablas.
# Nuestra tabla nueva no tiene ninguno de estos nodos, y no podemos agregar contenido a ella hasta que los tenga.
self.assertEqual(0, table.get_child_nodes(aw.NodeType.ANY, True).count)
# Llamar al método "EnsureMinimum" en una tabla garantizará que
# la tabla tiene al menos una fila y una celda con un párrafo vacío.
table.ensure_minimum()
table.first_row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

