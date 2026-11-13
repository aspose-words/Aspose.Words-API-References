---
title: Node.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Python
description: "Node.clone method. Creates a duplicate of the node."
type: docs
weight: 430
url: /es/python-net/aspose.words/node/clone/
---

## clone(is_clone_children) {#bool}

Creates a duplicate of the node.


```python
def clone(self, is_clone_children: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| is_clone_children | bool | True to recursively clone the subtree under the specified node;  false to clone only the node itself. |

### Remarks

This method serves as a copy constructor for nodes. 
The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The *isCloneChildren* parameter
specifies whether to perform copy all child nodes as well.




### Returns

The cloned node.


### Examples

Shows how to clone a composite node.

```python
doc = aw.Document()
para = doc.first_section.body.first_paragraph
para.append_child(aw.Run(doc=doc, text='Hello world!'))
# A continuación se presentan dos formas de clonar un nodo compuesto.
# 1 -  Crear una copia de un nodo, y crear también una copia de cada uno de sus nodos hijos.
clone_with_children = para.clone(True)
self.assertTrue(clone_with_children.as_composite_node().has_child_nodes)
self.assertEqual('Hello world!', clone_with_children.get_text().strip())
# 2 -  Crear una copia de un nodo solo, sin ningún hijo.
clone_without_children = para.clone(False)
self.assertFalse(clone_without_children.as_composite_node().has_child_nodes)
self.assertEqual('', clone_without_children.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

