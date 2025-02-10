---
title: Node.previous_pre_order method
linktitle: previous_pre_order method
articleTitle: previous_pre_order method
second_title: Aspose.Words for Python
description: "Node.previous_pre_order method. Gets the previous node according to the pre-order tree traversal algorithm."
type: docs
weight: 480
url: /python-net/aspose.words/node/previous_pre_order/
---

## previous_pre_order(root_node) {#node}

Gets the previous node according to the pre-order tree traversal algorithm.


```python
def previous_pre_order(self, root_node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| root_node | [Node](../) | The top node (limit) of traversal. |

### Returns

Previous node in pre-order order. Null if reached the *rootNode*.


### Examples

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
self.assertEqual(9, len(list(filter(lambda s: s.has_image, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))))))
cur_node = doc
while cur_node != None:
    next_node = cur_node.next_pre_order(doc)
    if cur_node.previous_pre_order(doc) != None and next_node != None:
        self.assertEqual(cur_node, next_node.previous_pre_order(doc))
    if cur_node.node_type == aw.NodeType.SHAPE and cur_node.as_shape().has_image:
        cur_node.remove()
    cur_node = next_node
self.assertEqual(0, len(list(filter(lambda s: s.has_image, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))))))
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

