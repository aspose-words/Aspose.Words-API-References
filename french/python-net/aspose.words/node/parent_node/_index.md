---
title: Node.parent_node property
linktitle: parent_node property
articleTitle: parent_node property
second_title: Aspose.Words for Python
description: "Node.parent_node property. Gets the immediate parent of this node."
type: docs
weight: 60
url: /fr/python-net/aspose.words/node/parent_node/
---

## Node.parent_node property

Gets the immediate parent of this node.


```python
@property
def parent_node(self) -> aspose.words.CompositeNode:
    ...

```

### Remarks

If a node has just been created and not yet added to the tree,
or if it has been removed from the tree, the parent is ``None``.




### Examples

Shows how to create a node and set its owning document.

```python
from api_example_base import ApiExampleBase
doc = aw.Document()
para = aw.Paragraph(doc)
para.append_child(aw.Run(doc=doc, text='Hello world!'))
# Nous n'avons pas encore ajouté ce paragraphe en tant qu'enfant à aucun nœud composite.
self.assertIsNone(para.parent_node)
# Si un nœud est d'un type d'enfant approprié d'un autre nœud composite,
# nous ne pouvons le joindre en tant qu'enfant que si les deux nœuds ont le même document propriétaire.
# Le document propriétaire est le document que nous avons passé au constructeur du nœud.
# Nous n'avons pas attaché ce paragraphe au document, donc le document ne contient pas son texte.
self.assertEqual(para.document, doc)
self.assertEqual('', doc.get_text().strip())
# Puisque le document possède ce paragraphe, nous pouvons appliquer l'un de ses styles au contenu du paragraphe.
para.paragraph_format.style = doc.styles.get_by_name('Heading 1')
# Ajoutez ce nœud au document, puis vérifiez son contenu.
doc.first_section.body.append_child(para)
self.assertEqual(doc.first_section.body, para.parent_node)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

