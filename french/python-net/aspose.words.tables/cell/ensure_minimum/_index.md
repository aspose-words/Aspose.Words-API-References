---
title: Cell.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Cell.ensure_minimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 160
url: /fr/python-net/aspose.words.tables/cell/ensure_minimum/
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
# Les cellules peuvent contenir des paragraphes avec des éléments typiques tels que des runs, des formes, et même d'autres tableaux.
# Notre nouvelle cellule ne possède aucun paragraphe, et nous ne pouvons pas ajouter de contenu tel que des nœuds de run et de forme tant qu'elle n'en a pas.
self.assertEqual(0, cell.get_child_nodes(aw.NodeType.ANY, True).count)
# Appeler la méthode "EnsureMinimum" sur une cellule garantira que
# la cellule possède au moins un paragraphe vide, auquel nous pourrons alors ajouter du contenu.
cell.ensure_minimum()
cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

