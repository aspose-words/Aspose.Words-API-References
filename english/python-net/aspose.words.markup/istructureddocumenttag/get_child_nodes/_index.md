---
title: IStructuredDocumentTag.get_child_nodes method
linktitle: get_child_nodes method
articleTitle: get_child_nodes method
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.get_child_nodes method. Returns a live collection of child nodes that match the specified types."
type: docs
weight: 170
url: /python-net/aspose.words.markup/istructureddocumenttag/get_child_nodes/
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

Shows how to remove structured document tag, but keeps content inside.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags.docx')
# This collection provides a unified interface for accessing ranged and non-ranged structured tags.
sdts = list(doc.range.structured_document_tags)
self.assertEqual(5, len(sdts))
# Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
for sdt in sdts:
    if sdt.get_child_nodes(aw.NodeType.ANY, False).count > 0:
        sdt.remove_self_only()
sdts = list(doc.range.structured_document_tags)
self.assertEqual(0, len(sdts))
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

