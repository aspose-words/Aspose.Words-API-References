---
title: ensure_minimum method
second_title: Aspose.Words for Python via .NET API Reference
description: "Ensures that the section has Body with one Paragraph."
type: docs
weight: 130
url: /python-net/aspose.words/section/ensure_minimum/
---

## ensure_minimum() {#default}

Ensures that the section has Body with one Paragraph.


```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to prepare a new section node for editing.

```python
doc = aw.Document()

# A blank document comes with a section, which has a body, which in turn has a paragraph.
# We can add contents to this document by adding elements such as text runs, shapes, or tables to that paragraph.
self.assertEqual(aw.NodeType.SECTION, doc.get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.BODY, doc.sections[0].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[0].body.get_child(aw.NodeType.ANY, 0, True).node_type)

# If we add a new section like this, it will not have a body, or any other child nodes.
doc.sections.add(aw.Section(doc))

self.assertEqual(0, doc.sections[1].get_child_nodes(aw.NodeType.ANY, True).count)

# Run the "ensure_minimum" method to add a body and a paragraph to this section to begin editing it.
doc.last_section.ensure_minimum()

self.assertEqual(aw.NodeType.BODY, doc.sections[1].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[1].body.get_child(aw.NodeType.ANY, 0, True).node_type)

doc.sections[0].body.first_paragraph.append_child(aw.Run(doc, "Hello world!"))

self.assertEqual("Hello world!", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

