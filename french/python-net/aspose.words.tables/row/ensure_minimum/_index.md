---
title: Row.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Row.ensure_minimum method. If the [Row](../) has no cells, creates and appends one [Cell](../../cell/)."
type: docs
weight: 160
url: /fr/python-net/aspose.words.tables/row/ensure_minimum/
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
# Les lignes contiennent des cellules, contenant des paragraphes avec des éléments typiques tels que des segments, des formes, et même d’autres tableaux.
# Notre nouvelle ligne ne contient aucun de ces nœuds, et nous ne pouvons pas ajouter de contenu tant qu'elle n'en a pas.
self.assertEqual(0, row.get_child_nodes(aw.NodeType.ANY, True).count)
# Appeler la méthode "EnsureMinimum" sur un tableau garantira que
# le tableau possède au moins une cellule avec un paragraphe vide.
row.ensure_minimum()
row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Row](../)

