---
title: DocumentBuilder.move_to method
linktitle: move_to method
articleTitle: move_to method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 490
url: /python-net/aspose.words/documentbuilder/move_to/
---

## move_to(node) {#node}

Moves the cursor to an inline node or to the end of a paragraph.


```python
def move_to(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node must be a paragraph or a direct child of a paragraph. |

### Remarks

When *node* is an inline-level node, the cursor is moved to this node
and further content will be inserted before that node.

When *node* is a [Paragraph](../../paragraph/), the cursor is moved to the end of the paragraph
and further content will be inserted just before the paragraph break.

When *node* is a block-level node but not a [Paragraph](../../paragraph/), the cursor is moved to the end of the first paragraph into block-level node
and further content will be inserted just before the paragraph break.




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

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Run 1. ")

# The document builder has a cursor, which acts as the part of the document
# where the builder appends new nodes when we use its document construction methods.
# This cursor functions in the same way as Microsoft Word's blinking cursor,
# and it also always ends up immediately after any node that the builder just inserted.
# To append content to a different part of the document,
# we can move the cursor to a different node with the "MoveTo" method.
builder.move_to(doc.first_section.body.first_paragraph.runs[0])

# The cursor is now in front of the node that we moved it to.
# Adding a second run will insert it in front of the first run.
builder.writeln("Run 2. ")

self.assertEqual("Run 2. \rRun 1.", doc.get_text().strip())

# Move the cursor to the end of the document to continue appending text to the end as before.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln("Run 3. ")

self.assertEqual("Run 2. \rRun 1. \rRun 3.", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

