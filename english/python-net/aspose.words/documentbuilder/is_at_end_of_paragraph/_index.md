---
title: DocumentBuilder.is_at_end_of_paragraph property
linktitle: is_at_end_of_paragraph property
articleTitle: is_at_end_of_paragraph property
second_title: Aspose.Words for Python
description: "DocumentBuilder.is_at_end_of_paragraph property. Returns ``True`` if the cursor is at the end of the current paragraph."
type: docs
weight: 110
url: /python-net/aspose.words/documentbuilder/is_at_end_of_paragraph/
---

## DocumentBuilder.is_at_end_of_paragraph property

Returns ``True`` if the cursor is at the end of the current paragraph.



### Examples

Shows how to move a document builder's cursor to different nodes in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
# and a bookmark end node.
builder.start_bookmark("MyBookmark")
builder.write("Bookmark contents.")
builder.end_bookmark("MyBookmark")

first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)

self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual("Bookmark contents.", first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)

# The document builder's cursor is always ahead of the node that we last added with it.
# If the builder's cursor is at the end of the document, its current node will be "None".
# The previous node is the bookmark end node that we last added.
# Adding new nodes with the builder will append them to the last node.
self.assertIsNone(builder.current_node)

# If we wish to edit a different part of the document with the builder,
# we will need to bring its cursor to the node we wish to edit.
builder.move_to_bookmark("MyBookmark")

# Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
self.assertEqual(first_paragraph_nodes[1], builder.current_node)

# We can also move the cursor to an individual node like this.
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])

self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)

# We can use specific methods to move to the start/end of a document.
builder.move_to_document_end()

self.assertTrue(builder.is_at_end_of_paragraph)

builder.move_to_document_start()

self.assertTrue(builder.is_at_start_of_paragraph)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

