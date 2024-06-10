---
title: CompositeNode.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "CompositeNode.count property. Gets the number of immediate children of this node."
type: docs
weight: 10
url: /python-net/aspose.words/compositenode/count/
---

## CompositeNode.count property

Gets the number of immediate children of this node.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```python
doc = aw.Document()
# An empty document, by default, has one paragraph.
self.assertEqual(1, doc.first_section.body.paragraphs.count)
# Composite nodes such as our paragraph can contain other composite and inline nodes as children.
paragraph = doc.first_section.body.first_paragraph
paragraph_text = aw.Run(doc=doc, text='Initial text. ')
paragraph.append_child(paragraph_text)
# Create three more run nodes.
run1 = aw.Run(doc=doc, text='Run 1. ')
run2 = aw.Run(doc=doc, text='Run 2. ')
run3 = aw.Run(doc=doc, text='Run 3. ')
# The document body will not display these runs until we insert them into a composite node
# that itself is a part of the document's node tree, as we did with the first run.
# We can determine where the text contents of nodes that we insert
# appears in the document by specifying an insertion location relative to another node in the paragraph.
self.assertEqual('Initial text.', paragraph.get_text().strip())
# Insert the second run into the paragraph in front of the initial run.
paragraph.insert_before(run2, paragraph_text)
self.assertEqual('Run 2. Initial text.', paragraph.get_text().strip())
# Insert the third run after the initial run.
paragraph.insert_after(run3, paragraph_text)
self.assertEqual('Run 2. Initial text. Run 3.', paragraph.get_text().strip())
# Insert the first run to the start of the paragraph's child nodes collection.
paragraph.prepend_child(run1)
self.assertEqual('Run 1. Run 2. Initial text. Run 3.', paragraph.get_text().strip())
self.assertEqual(4, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
# We can modify the contents of the run by editing and deleting existing child nodes.
paragraph.get_child_nodes(aw.NodeType.RUN, True)[1].as_run().text = 'Updated run 2. '
paragraph.get_child_nodes(aw.NodeType.RUN, True).remove(paragraph_text)
self.assertEqual('Run 1. Updated run 2. Run 3.', paragraph.get_text().strip())
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

