---
title: start_editable_range method
second_title: Aspose.Words for Python via .NET API Reference
description: "Marks the current position in the document as an editable range start."
type: docs
weight: 600
url: /python-net/aspose.words/documentbuilder/start_editable_range/
---

## start_editable_range() {#default}

Marks the current position in the document as an editable range start.


```python
def start_editable_range(self):
    ...
```

Editable range in a document can overlap and span any range. To create a valid editable range you need to
call both [DocumentBuilder.start_editable_range()](./#default) and [DocumentBuilder.end_editable_range()](../end_editable_range/#default)
or [DocumentBuilder.end_editable_range()](../end_editable_range/#editablerangestart) methods.

Badly formed editable range will be ignored when the document is saved.




### Returns

The editable range start node that was just created.


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

Shows how to create nested editable ranges.

```python
doc = aw.Document()
doc.protect(aw.ProtectionType.READ_ONLY, "MyPassword")

builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.")

# Create two nested editable ranges.
outer_editable_range_start = builder.start_editable_range()
builder.writeln("This paragraph inside the outer editable range and can be edited.")

inner_editable_range_start = builder.start_editable_range()
builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.")

# Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
# When we want to end an editable range in this situation,
# we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
builder.end_editable_range(inner_editable_range_start)

builder.writeln("This paragraph inside the outer editable range and can be edited.")

builder.end_editable_range(outer_editable_range_start)

builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.")

# If a region of text has two overlapping editable ranges with specified groups,
# the combined group of users excluded by both groups are prevented from editing it.
outer_editable_range_start.editable_range.editor_group = aw.EditorType.EVERYONE
inner_editable_range_start.editable_range.editor_group = aw.EditorType.CONTRIBUTORS

doc.save(ARTIFACTS_DIR + "EditableRange.nested.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

