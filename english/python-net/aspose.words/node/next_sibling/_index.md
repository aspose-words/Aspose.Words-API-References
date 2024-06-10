---
title: Node.next_sibling property
linktitle: next_sibling property
articleTitle: next_sibling property
second_title: Aspose.Words for Python
description: "Node.next_sibling property. Gets the node immediately following this node."
type: docs
weight: 40
url: /python-net/aspose.words/node/next_sibling/
---

## Node.next_sibling property

Gets the node immediately following this node.


```python
@property
def next_sibling(self) -> aspose.words.Node:
    ...

```

### Remarks

If there is no next node, a ``None`` is returned.



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

