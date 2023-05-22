---
title: Node.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "Node.document property. Gets the document to which this node belongs."
type: docs
weight: 20
url: /python-net/aspose.words/node/document/
---

## Node.document property

Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created
and not yet added to the tree, or if it has been removed from the tree.




### Examples

Shows how to create a node and set its owning document.

```python
doc = aw.Document()
para = aw.Paragraph(doc)
para.append_child(aw.Run(doc, "Hello world!"))

# We have not yet appended this paragraph as a child to any composite node.
self.assertIsNone(para.parent_node)

# If a node is an appropriate child node type of another composite node,
# we can attach it as a child only if both nodes have the same owner document.
# The owner document is the document we passed to the node's constructor.
# We have not attached this paragraph to the document, so the document does not contain its text.
self.assertEqual(para.document, doc)
self.assertEqual("", doc.get_text().strip())

# Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
para.paragraph_format.style = doc.styles.get_by_name("Heading 1")

# Add this node to the document, and then verify its contents.
doc.first_section.body.append_child(para)

self.assertEqual(doc.first_section.body, para.parent_node)
self.assertEqual("Hello world!", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

