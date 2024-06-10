---
title: Node.node_type_to_string method
linktitle: node_type_to_string method
articleTitle: node_type_to_string method
second_title: Aspose.Words for Python
description: "Node.node_type_to_string method. A utility method that converts a node type enum value into a user friendly string."
type: docs
weight: 470
url: /python-net/aspose.words/node/node_type_to_string/
---

## node_type_to_string(node_type) {#nodetype}

A utility method that converts a node type enum value into a user friendly string.


```python
def node_type_to_string(self, node_type: aspose.words.NodeType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node_type | [NodeType](../../nodetype/) |  |

### Examples

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

