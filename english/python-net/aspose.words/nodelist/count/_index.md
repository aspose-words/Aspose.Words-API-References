---
title: NodeList.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "NodeList.count property. Gets the number of nodes in the list."
type: docs
weight: 20
url: /python-net/aspose.words/nodelist/count/
---

## NodeList.count property

Gets the number of nodes in the list.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to use XPaths to navigate a NodeList.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert some nodes with a DocumentBuilder.
builder.writeln("Hello world!")

builder.start_table()
builder.insert_cell()
builder.write("Cell 1")
builder.insert_cell()
builder.write("Cell 2")
builder.end_table()

builder.insert_image(drawing.Image.from_file(IMAGE_DIR + "Logo.jpg"))

# Our document contains three Run nodes.
node_list = doc.select_nodes("//Run")

self.assertEqual(3, node_list.count)
self.assertTrue(any(node.get_text().strip() == "Hello world!" for node in node_list))
self.assertTrue(any(node.get_text().strip() == "Cell 1" for node in node_list))
self.assertTrue(any(node.get_text().strip() == "Cell 2" for node in node_list))

# Use a double forward slash to select all Run nodes
# that are indirect descendants of a Table node, which would be the runs inside the two cells we inserted.
node_list = doc.select_nodes("//Table//Run")

self.assertEqual(2, node_list.count)
self.assertTrue(any(node.get_text().strip() == "Cell 1" for node in node_list))
self.assertTrue(any(node.get_text().strip() == "Cell 2" for node in node_list))

# Single forward slashes specify direct descendant relationships,
# which we skipped when we used double slashes.
self.assertEqual(
    doc.select_nodes("//Table//Run"),
    doc.select_nodes("//Table/Row/Cell/Paragraph/Run"))

# Access the shape that contains the image we inserted.
node_list = doc.select_nodes("//Shape")

self.assertEqual(1, node_list.count)

shape = node_list[0].as_shape()
self.assertTrue(shape.has_image)
```

### See Also

* module [aspose.words](../../)
* class [NodeList](../)

