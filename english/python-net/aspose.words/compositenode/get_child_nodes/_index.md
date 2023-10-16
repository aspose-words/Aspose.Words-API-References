---
title: CompositeNode.get_child_nodes method
linktitle: get_child_nodes method
articleTitle: get_child_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.get_child_nodes method. Returns a live collection of child nodes that match the specified type."
type: docs
weight: 100
url: /python-net/aspose.words/compositenode/get_child_nodes/
---

## get_child_nodes(node_type, is_deep) {#nodetype_bool}

Returns a live collection of child nodes that match the specified type.


```python
def get_child_nodes(self, node_type: aspose.words.NodeType, is_deep: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node_type | [NodeType](../../nodetype/) |  |
| is_deep | bool |  |

The collection of nodes returned by this method is always live.




### Returns

A live collection of child nodes of the specified type.


### Examples

Shows how to print all of a document's comments and their replies.

```python
doc = aw.Document(MY_DIR + "Comments.docx")

comments = doc.get_child_nodes(aw.NodeType.COMMENT, True)

# If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
# Print all top-level comments along with any replies they may have.
for comment in comments:
    comment = comment.as_comment()
    if comment.ancestor is None:
        print("Top-level comment:")
        print(f"\t\"{comment.get_text().strip()}\", by {comment.author}")
        print(f"Has {comment.replies.count} replies")
        for comment_reply in comment.replies:
            comment_reply = comment_reply.as_comment()
            print(f"\t\"{comment_reply.get_text().strip()}\", by {comment_reply.author}")
        print()
```

Shows how to extract images from a document, and save them to the local file system as individual files.

```python
doc = aw.Document(MY_DIR + "Images.docx")

# Get the collection of shapes from the document,
# and save the image data of every shape with an image as a file to the local file system.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)

self.assertEqual(9, len([s for s in shapes if s.as_shape().has_image]))

image_index = 0
for shape in shapes:
    shape = shape.as_shape()

    if shape.has_image:

        # The image data of shapes may contain images of many possible image formats.
        # We can determine a file extension for each image automatically, based on its format.
        image_file_name = f"File.extract_images.{image_index}{aw.FileFormatUtil.image_type_to_extension(shape.image_data.image_type)}"
        shape.image_data.save(ARTIFACTS_DIR + image_file_name)
        image_index += 1
```

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```python
doc = aw.Document()

# An empty document, by default, has one paragraph.
self.assertEqual(1, doc.first_section.body.paragraphs.count)

# Composite nodes such as our paragraph can contain other composite and inline nodes as children.
paragraph = doc.first_section.body.first_paragraph
paragraph_text = aw.Run(doc, "Initial text. ")
paragraph.append_child(paragraph_text)

# Create three more run nodes.
run1 = aw.Run(doc, "Run 1. ")
run2 = aw.Run(doc, "Run 2. ")
run3 = aw.Run(doc, "Run 3. ")

# The document body will not display these runs until we insert them into a composite node
# that itself is a part of the document's node tree, as we did with the first run.
# We can determine where the text contents of nodes that we insert
# appears in the document by specifying an insertion location relative to another node in the paragraph.
self.assertEqual("Initial text.", paragraph.get_text().strip())

# Insert the second run into the paragraph in front of the initial run.
paragraph.insert_before(run2, paragraph_text)

self.assertEqual("Run 2. Initial text.", paragraph.get_text().strip())

# Insert the third run after the initial run.
paragraph.insert_after(run3, paragraph_text)

self.assertEqual("Run 2. Initial text. Run 3.", paragraph.get_text().strip())

# Insert the first run to the start of the paragraph's child nodes collection.
paragraph.prepend_child(run1)

self.assertEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.get_text().strip())
self.assertEqual(4, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)

# We can modify the contents of the run by editing and deleting existing child nodes.
paragraph.get_child_nodes(aw.NodeType.RUN, True)[1].as_run().text = "Updated run 2. "
paragraph.get_child_nodes(aw.NodeType.RUN, True).remove(paragraph_text)

self.assertEqual("Run 1. Updated run 2. Run 3.", paragraph.get_text().strip())
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

