---
title: CompositeNode.first_child property
linktitle: first_child property
articleTitle: first_child property
second_title: Aspose.Words for Python
description: "CompositeNode.first_child property. Gets the first child of the node."
type: docs
weight: 20
url: /python-net/aspose.words/compositenode/first_child/
---

## CompositeNode.first_child property

Gets the first child of the node.


```python
@property
def first_child(self) -> aspose.words.Node:
    ...

```

### Remarks

If there is no first child node, a ``None`` is returned.



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
* class [CompositeNode](../)

