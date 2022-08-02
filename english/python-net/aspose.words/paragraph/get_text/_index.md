---
title: get_text method
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the text of this paragraph including the end of paragraph character."
type: docs
weight: 260
url: /python-net/aspose.words/paragraph/get_text/
---

## get_text() {#default}

Gets the text of this paragraph including the end of paragraph character.


```python
def get_text(self):
    ...
```

The text of all child nodes is concatenated and the end of paragraph character is appended as follows:


* If the paragraph is the last paragraph of [Body](../../body/), then
  [ControlChar.SECTION_BREAK](../../controlchar/SECTION_BREAK/) (\\x000c) is appended.
  
* If the paragraph is the last paragraph of [Cell](../../../aspose.words.tables/cell/), then
  [ControlChar.CELL](../../controlchar/CELL/) (\\x0007) is appended.
  
* For all other paragraphs
  [ControlChar.PARAGRAPH_BREAK](../../controlchar/PARAGRAPH_BREAK/) (\\r) is appended.
  
The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




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
* class [Paragraph](../)

