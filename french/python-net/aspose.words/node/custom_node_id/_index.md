---
title: Node.custom_node_id property
linktitle: custom_node_id property
articleTitle: custom_node_id property
second_title: Aspose.Words for Python
description: "Node.custom_node_id property. Specifies custom node identifier."
type: docs
weight: 10
url: /fr/python-net/aspose.words/node/custom_node_id/
---

## Node.custom_node_id property

Specifies custom node identifier.


```python
@property
def custom_node_id(self) -> int:
    ...

@custom_node_id.setter
def custom_node_id(self, value: int):
    ...

```

### Remarks

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.




### Examples

Shows how to traverse through a composite node's collection of child nodes.

```python
doc = aw.Document()
# Ajoutez deux exécutions et une forme en tant que nœuds enfants au premier paragraphe de ce document.
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
paragraph.append_child(aw.Run(doc=doc, text='Hello world! '))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
# Notez que le 'CustomNodeId' n'est pas enregistré dans un fichier de sortie et n'existe que pendant la durée de vie du nœud.
shape.custom_node_id = 100
shape.wrap_type = aw.drawing.WrapType.INLINE
paragraph.append_child(shape)
paragraph.append_child(aw.Run(doc=doc, text='Hello again!'))
# Itérer à travers la collection d'enfants immédiats du paragraphe,
# et imprimer toutes les exécutions ou formes que nous trouvons à l'intérieur.
children = paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, False).count)
for child in children:
    switch_condition = child.node_type
    if switch_condition == aw.NodeType.RUN:
        print('Run contents:')
        print(f'\t"{child.get_text().strip()}"')
    elif switch_condition == aw.NodeType.SHAPE:
        child_shape = child.as_shape()
        print('Shape:')
        print(f'\t{child_shape.shape_type}, {child_shape.width}x{child_shape.height}')
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

