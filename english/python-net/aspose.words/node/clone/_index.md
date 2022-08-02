---
title: clone method
second_title: Aspose.Words for Python via .NET API Reference
description: "Creates a duplicate of the node."
type: docs
weight: 430
url: /python-net/aspose.words/node/clone/
---

## clone(is_clone_children) {#bool}

Creates a duplicate of the node.


```python
def clone(self, is_clone_children: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| is_clone_children | bool |  |

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
para.append_child(aw.Run(doc, "Hello world!"))

# Below are two ways of cloning a composite node.
# 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
clone_with_children = para.clone(True)

self.assertTrue(clone_with_children.as_composite_node().has_child_nodes)
self.assertEqual("Hello world!", clone_with_children.get_text().strip())

# 2 -  Create a clone of a node just by itself without any children.
clone_without_children = para.clone(False)

self.assertFalse(clone_without_children.as_composite_node().has_child_nodes)
self.assertEqual("", clone_without_children.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

