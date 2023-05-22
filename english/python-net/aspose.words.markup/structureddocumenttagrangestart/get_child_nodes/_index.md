---
title: StructuredDocumentTagRangeStart.get_child_nodes method
linktitle: get_child_nodes method
articleTitle: get_child_nodes method
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeStart.get_child_nodes method. Returns a live collection of child nodes that match the specified types."
type: docs
weight: 210
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/get_child_nodes/
---

## get_child_nodes(node_type, is_deep) {#nodetype_bool}

Returns a live collection of child nodes that match the specified types.


```python
def get_child_nodes(self, node_type: aspose.words.NodeType, is_deep: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node_type | [NodeType](../../../aspose.words/nodetype/) |  |
| is_deep | bool |  |

### Examples

Shows how to get child nodes of StructuredDocumentTagRangeStart.

```python
doc = aw.Document(MY_DIR + "Multi-section structured document tags.docx")
tag = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, True)[0].as_structured_document_tag_range_start()

print("StructuredDocumentTagRangeStart values:")
print(f"\t|Child nodes count: {tag.child_nodes.count}\n")

for node in tag.child_nodes:
    print(f"\t|Child node type: {node.node_type}")

for node in tag.get_child_nodes(aw.NodeType.RUN, True):
    print(f"\t|Child node text: {node.get_text()}")
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagRangeStart](../)

