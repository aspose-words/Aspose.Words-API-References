---
title: Table.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Table.ensure_minimum method. If the table has no rows, creates and appends one [Row](../../row/)."
type: docs
weight: 420
url: /fr/python-net/aspose.words.tables/table/ensure_minimum/
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
# Les tables contiennent des lignes, qui contiennent des cellules, qui peuvent contenir des paragraphes
# avec des éléments typiques tels que des exécutions, des formes et même d'autres tableaux.
# Notre nouvelle table ne possède aucun de ces nœuds, et nous ne pouvons pas y ajouter de contenu tant qu’elle n’en a pas.
self.assertEqual(0, table.get_child_nodes(aw.NodeType.ANY, True).count)
# Appeler la méthode "EnsureMinimum" sur un tableau garantira que
# la table possède au moins une ligne et une cellule avec un paragraphe vide.
table.ensure_minimum()
table.first_row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

