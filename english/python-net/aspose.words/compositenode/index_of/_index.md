---
title: CompositeNode.index_of method
linktitle: index_of method
articleTitle: index_of method
second_title: Aspose.Words for Python
description: "CompositeNode.index_of method. Returns the index of the specified child node in the child node array."
type: docs
weight: 110
url: /python-net/aspose.words/compositenode/index_of/
---

## index_of(child) {#node}

Returns the index of the specified child node in the child node array.


```python
def index_of(self, child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../node/) |  |

Returns -1 if the node is not found in the child nodes.


### Examples

Shows how to get the index of a given child node from its parent.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

body = doc.first_section.body

# Retrieve the index of the last paragraph in the body of the first section.
self.assertEqual(24, body.get_child_nodes(aw.NodeType.ANY, False).index_of(body.last_paragraph))
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

