---
title: move_to_bookmark method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.DocumentBuilder.move_to_bookmark method"
type: docs
weight: 470
url: /python-net/aspose.words/documentbuilder/move_to_bookmark/
---

## move_to_bookmark(bookmark_name) {#str}

Moves the cursor to a bookmark.


```python
def move_to_bookmark(self, bookmark_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmark_name | str |  |

Moves the cursor to a position just after the start of the bookmark with the
specified name.

The comparison is not case-sensitive. If the bookmark was not found, false is
returned and the cursor is not moved.

Inserting new text does not replace existing text of the bookmark.

Note that some bookmarks in the document are assigned to form fields.
Moving to such a bookmark and inserting text there inserts the text into the
form field code. Although this will not invalidate the form field, the inserted
text will not be visible because it becomes part of the field code.




### Returns

True if the bookmark was found; false otherwise.


## move_to_bookmark(bookmark_name, is_start, is_after) {#str_bool_bool}

Moves the cursor to a bookmark with greater precision.


```python
def move_to_bookmark(self, bookmark_name: str, is_start: bool, is_after: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmark_name | str |  |
| is_start | bool |  |
| is_after | bool |  |

Moves the cursor to a position before or after the bookmark start or end.

If desired position is not at inline level, moves to the next paragraph.

The comparison is not case-sensitive. If the bookmark was not found, false is
returned and the cursor is not moved.




### Returns

True if the bookmark was found; false otherwise.


## Examples

Shows how to move a document builder's cursor to different nodes in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
# and a bookmark end node.
builder.start_bookmark("MyBookmark")
builder.write("Bookmark contents.")
builder.end_bookmark("MyBookmark")

first_paragraph_nodes = doc.first_section.body.first_paragraph.child_nodes

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

Shows how to move a document builder's node insertion point cursor to a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# A valid bookmark consists of a BookmarkStart node, a BookmarkEnd node with a
# matching bookmark name somewhere afterward, and contents enclosed by those nodes.
builder.start_bookmark("MyBookmark")
builder.write("Hello world! ")
builder.end_bookmark("MyBookmark")

# There are 4 ways of moving a document builder's cursor to a bookmark.
# If we are between the BookmarkStart and BookmarkEnd nodes, the cursor will be inside the bookmark.
# This means that any text added by the builder will become a part of the bookmark.
# 1 -  Outside of the bookmark, in front of the BookmarkStart node:
self.assertTrue(builder.move_to_bookmark("MyBookmark", True, False))
builder.write("1. ")

self.assertEqual("Hello world! ", doc.range.bookmarks.get_by_name("MyBookmark").text)
self.assertEqual("1. Hello world!", doc.get_text().strip())

# 2 -  Inside the bookmark, right after the BookmarkStart node:
self.assertTrue(builder.move_to_bookmark("MyBookmark", True, True))
builder.write("2. ")

self.assertEqual("2. Hello world! ", doc.range.bookmarks.get_by_name("MyBookmark").text)
self.assertEqual("1. 2. Hello world!", doc.get_text().strip())

# 2 -  Inside the bookmark, right in front of the BookmarkEnd node:
self.assertTrue(builder.move_to_bookmark("MyBookmark", False, False))
builder.write("3. ")

self.assertEqual("2. Hello world! 3. ", doc.range.bookmarks.get_by_name("MyBookmark").text)
self.assertEqual("1. 2. Hello world! 3.", doc.get_text().strip())

# 4 -  Outside of the bookmark, after the BookmarkEnd node:
self.assertTrue(builder.move_to_bookmark("MyBookmark", False, True))
builder.write("4.")

self.assertEqual("2. Hello world! 3. ", doc.range.bookmarks.get_by_name("MyBookmark").text)
self.assertEqual("1. 2. Hello world! 3. 4.", doc.get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

