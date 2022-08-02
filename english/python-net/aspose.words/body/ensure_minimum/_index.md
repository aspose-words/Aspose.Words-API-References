---
title: ensure_minimum method
second_title: Aspose.Words for Python via .NET API Reference
description: "If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 50
url: /python-net/aspose.words/body/ensure_minimum/
---

## ensure_minimum() {#default}

If the last child is not a paragraph, creates and appends one empty paragraph.


```python
def ensure_minimum(self):
    ...
```

### Examples

Clears main text from all sections from the document leaving the sections themselves.

```python
doc = aw.Document()

# A blank document contains one section, one body and one paragraph.
# Call the "remove_all_children" method to remove all those nodes,
# and end up with a document node with no children.
doc.remove_all_children()

# This document now has no composite child nodes that we can add content to.
# If we wish to edit it, we will need to repopulate its node collection.
# First, create a new section, and then append it as a child to the root document node.
section = aw.Section(doc)
doc.append_child(section)

# A section needs a body, which will contain and display all its contents
# on the page between the section's header and footer.
body = aw.Body(doc)
section.append_child(body)

# This body has no children, so we cannot add runs to it yet.
self.assertEqual(0, doc.first_section.body.get_child_nodes(aw.NodeType.ANY, True).count)

# Call the "ensure_minimum" to make sure that this body contains at least one empty paragraph.
body.ensure_minimum()

# Now, we can add runs to the body, and get the document to display them.
body.first_paragraph.append_child(aw.Run(doc, "Hello world!"))

self.assertEqual("Hello world!", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Body](../)

