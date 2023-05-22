---
title: StructuredDocumentTag.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.clear method. Clears contents of this structured document tag and displays a placeholder if it is defined."
type: docs
weight: 340
url: /python-net/aspose.words.markup/structureddocumenttag/clear/
---

## clear() {#default}

Clears contents of this structured document tag and displays a placeholder if it is defined.


```python
def clear(self):
    ...
```

It is not possible to clear contents of a structured document tag if it has revisions.

If this structured document tag is mapped to custom XML (with using the [StructuredDocumentTag.xml_mapping](../xml_mapping/)
property), the referenced XML node is cleared.




### Examples

Shows how to delete contents of structured document tag elements.

```python
doc = aw.Document()

# Create a plain text structured document tag, and then append it to the document.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)
doc.first_section.body.append_child(tag)

# This structured document tag, which is in the form of a text box, already displays placeholder text.
self.assertEqual("Click here to enter text.", tag.get_text().strip())
self.assertTrue(tag.is_showing_placeholder_text)

# Create a building block with text contents.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = "My placeholder"
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.ensure_minimum()
substitute_block.first_section.body.first_paragraph.append_child(aw.Run(glossary_doc, "Custom placeholder text."))
glossary_doc.append_child(substitute_block)

# Set the structured document tag's "placeholder_name" property to our building block's name to get
# the structured document tag to display the contents of the building block in place of the original default text.
tag.placeholder_name = "My placeholder"

self.assertEqual("Custom placeholder text.", tag.get_text().strip())
self.assertTrue(tag.is_showing_placeholder_text)

# Edit the text of the structured document tag and hide the placeholder text.
run = tag.get_child(aw.NodeType.RUN, 0, True).as_run()
run.text = "New text."
tag.is_showing_placeholder_text = False

self.assertEqual("New text.", tag.get_text().strip())

# Use the "clear" method to clear this structured document tag's contents and display the placeholder again.
tag.clear()

self.assertTrue(tag.is_showing_placeholder_text)
self.assertEqual("Custom placeholder text.", tag.get_text().strip())
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

