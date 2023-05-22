---
title: Document.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Document.ensure_minimum method. If the document contains no sections, creates one section with one paragraph."
type: docs
weight: 580
url: /python-net/aspose.words/document/ensure_minimum/
---

## ensure_minimum() {#default}

If the document contains no sections, creates one section with one paragraph.


```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to ensure that a document contains the minimal set of nodes required for editing its contents.

```python
# A newly created document contains one child Section, which includes one child Body and one child Paragraph.
# We can edit the document body's contents by adding nodes such as Runs or inline Shapes to that paragraph.
doc = aw.Document()
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)

self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(doc, nodes[0].parent_node)

self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(nodes[0], nodes[1].parent_node)

self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
self.assertEqual(nodes[1], nodes[2].parent_node)

# This is the minimal set of nodes that we need to be able to edit the document.
# We will no longer be able to edit the document if we remove any of them.
doc.remove_all_children()

self.assertEqual(0, doc.get_child_nodes(aw.NodeType.ANY, True).count)

# Call this method to make sure that the document has at least those three nodes so we can edit it again.
doc.ensure_minimum()

self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)

nodes[2].as_paragraph().runs.add(aw.Run(doc, "Hello world!"))
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

