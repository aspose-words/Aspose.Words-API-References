---
title: CompositeNode.has_child_nodes property
linktitle: has_child_nodes property
articleTitle: has_child_nodes property
second_title: Aspose.Words for Python
description: "CompositeNode.has_child_nodes property. Returns ``True`` if this node has any child nodes."
type: docs
weight: 30
url: /fr/python-net/aspose.words/compositenode/has_child_nodes/
---

## CompositeNode.has_child_nodes property

Returns ``True`` if this node has any child nodes.



```python
@property
def has_child_nodes(self) -> bool:
    ...

```

### Examples

Shows how to combine the rows from two tables into one.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
# Voici deux façons d'obtenir une table à partir d'un document.
# 1 -  Depuis la collection "Tables" d'un nœud Body :
first_table = doc.first_section.body.tables[0]
# 2 -  En utilisant la méthode "GetChild" :
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()
# Ajoutez toutes les lignes de la table actuelle à la suivante.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)
# Supprimez le conteneur de table vide.
second_table.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Table.CombineTables.docx')
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

