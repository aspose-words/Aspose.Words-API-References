---
title: Node.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "Node.node_type property. Gets the type of this node."
type: docs
weight: 50
url: /python-net/aspose.words/node/node_type/
---

## Node.node_type property

Gets the type of this node.


```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to remove all child nodes of a specific type from a composite node.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
self.assertEqual(2, doc.get_child_nodes(aw.NodeType.TABLE, True).count)
cur_node = doc.first_section.body.first_child
while cur_node != None:
    # Save the next sibling node as a variable in case we want to move to it after deleting this node.
    next_node = cur_node.next_sibling
    # A section body can contain Paragraph and Table nodes.
    # If the node is a Table, remove it from the parent.
    if cur_node.node_type == aw.NodeType.TABLE:
        cur_node.remove()
    cur_node = next_node
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.TABLE, True).count)
```

Shows how to use a node's next_sibling property to enumerate through its immediate children.

```python
doc = aw.Document(MY_DIR + 'Paragraphs.docx')
node = doc.first_section.body.first_child
while node is not None:
    print()
    print('Node type:', aw.Node.node_type_to_string(node.node_type))
    contents = node.get_text().strip()
    print('This node contains no text' if contents == '' else f'Contents: "{node.get_text().strip()}"')
    node = node.next_sibling
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

