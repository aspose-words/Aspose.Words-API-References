---
title: node_type property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns [NodeType.EDITABLE_RANGE_START](../../nodetype/#EDITABLE_RANGE_START)."
type: docs
weight: 30
url: /python-net/aspose.words/editablerangestart/node_type/
---

## EditableRangeStart.node_type property

Returns [NodeType.EDITABLE_RANGE_START](../../nodetype/#EDITABLE_RANGE_START).



### Examples

Shows how to work with an editable range.

```python
doc = aw.Document()
doc.protect(aw.ProtectionType.READ_ONLY, "MyPassword")

builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.")

# Editable ranges allow us to leave parts of protected documents open for editing.
editable_range_start = builder.start_editable_range()
builder.writeln("This paragraph is inside an editable range, and can be edited.")
editable_range_end = builder.end_editable_range()

# A well-formed editable range has a start node, and end node.
# These nodes have matching IDs and encompass editable nodes.
editable_range = editable_range_start.editable_range

self.assertEqual(editable_range_start.id, editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.id)

# Different parts of the editable range link to each other.
self.assertEqual(editable_range_start.id, editable_range.editable_range_start.id)
self.assertEqual(editable_range_start.id, editable_range_end.editable_range_start.id)
self.assertEqual(editable_range.id, editable_range_start.editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.editable_range_end.id)

# We can access the node types of each part like this. The editable range itself is not a node,
# but an entity which consists of a start, an end, and their enclosed contents.
self.assertEqual(aw.NodeType.EDITABLE_RANGE_START, editable_range_start.node_type)
self.assertEqual(aw.NodeType.EDITABLE_RANGE_END, editable_range_end.node_type)

builder.writeln("This paragraph is outside the editable range, and cannot be edited.")

doc.save(ARTIFACTS_DIR + "EditableRange.create_and_remove.docx")

# Remove an editable range. All the nodes that were inside the range will remain intact.
editable_range.remove()
```

### See Also

* module [aspose.words](../../)
* class [EditableRangeStart](../)

