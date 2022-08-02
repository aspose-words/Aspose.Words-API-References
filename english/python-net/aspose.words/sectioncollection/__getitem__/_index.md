---
title: SectionCollection indexer
second_title: Aspose.Words for Python via .NET API Reference
description: "Retrieves a section at the given index."
type: docs
weight: 10
url: /python-net/aspose.words/sectioncollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a section at the given index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows when to recalculate the page layout of the document.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# Saving a document to PDF, to an image, or printing for the first time will automatically
# cache the layout of the document within its pages.
doc.save(ARTIFACTS_DIR + "Document.update_page_layout.1.pdf")

# Modify the document in some way.
doc.styles.get_by_name("Normal").font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE

# In the current version of Aspose.Words, modifying the document does not automatically rebuild
# the cached page layout. If we wish for the cached layout
# to stay up to date, we will need to update it manually.
doc.update_page_layout()

doc.save(ARTIFACTS_DIR + "Document.update_page_layout.2.pdf")
```

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
* class [SectionCollection](../)

