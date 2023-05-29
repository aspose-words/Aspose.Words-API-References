---
title: CompositeNode.insert_before method
linktitle: insert_before method
articleTitle: insert_before method
second_title: Aspose.Words for Python
description: "CompositeNode.insert_before method. Inserts the specified node immediately before the specified reference node."
type: docs
weight: 130
url: /python-net/aspose.words/compositenode/insert_before/
---

## insert_before(new_child, ref_child) {#node_node}

Inserts the specified node immediately before the specified reference node.


```python
def insert_before(self, new_child: aspose.words.Node, ref_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_child | [Node](../../node/) |  |
| ref_child | [Node](../../node/) |  |

If  is``None``, inserts  at the end of the list of child nodes.




If the  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The inserted node.


### Examples

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

