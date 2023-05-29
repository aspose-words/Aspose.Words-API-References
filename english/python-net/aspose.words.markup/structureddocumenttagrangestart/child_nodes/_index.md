---
title: StructuredDocumentTagRangeStart.child_nodes property
linktitle: child_nodes property
articleTitle: child_nodes property
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeStart.child_nodes property. Gets all nodes between this range start node and the range end node."
type: docs
weight: 20
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/child_nodes/
---

## StructuredDocumentTagRangeStart.child_nodes property

Gets all nodes between this range start node and the range end node.


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

