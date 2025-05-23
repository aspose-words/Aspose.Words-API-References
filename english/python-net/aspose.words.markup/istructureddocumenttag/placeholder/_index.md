﻿---
title: IStructuredDocumentTag.placeholder property
linktitle: placeholder property
articleTitle: placeholder property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.placeholder property. Gets the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty,  the associated mapped XML element is empty as specified via the [IStructuredDocumentTag.xml_mapping](../xml_mapping/) element or the [IStructuredDocumentTag.is_showing_placeholder_text](../is_showing_placeholder_text/) element is true."
type: docs
weight: 100
url: /python-net/aspose.words.markup/istructureddocumenttag/placeholder/
---

## IStructuredDocumentTag.placeholder property

Gets the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, 
the associated mapped XML element is empty as specified via the [IStructuredDocumentTag.xml_mapping](../xml_mapping/) element
or the [IStructuredDocumentTag.is_showing_placeholder_text](../is_showing_placeholder_text/) element is true. 



```python
@property
def placeholder(self) -> aspose.words.buildingblocks.BuildingBlock:
    ...

```

### Remarks

Can be null, meaning that the placeholder is not applicable for this Sdt.


### Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```python
doc = aw.Document()
# Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
# The contents that it will display by default are a "Click here to enter text." prompt.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# We can get the tag to display the contents of a building block instead of the default text.
# First, add a building block with contents to the glossary document.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'Custom Placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.append_child(aw.Body(glossary_doc))
substitute_block.first_section.body.append_paragraph('Custom placeholder text.')
glossary_doc.append_child(substitute_block)
# Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
tag.placeholder_name = 'Custom Placeholder'
# If "PlaceholderName" refers to an existing block in the parent document's glossary document,
# we will be able to verify the building block via the "Placeholder" property.
self.assertEqual(substitute_block, tag.placeholder)
# Set the "IsShowingPlaceholderText" property to "true" to treat the
# structured document tag's current contents as placeholder text.
# This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
# Set the "IsShowingPlaceholderText" property to "false" to get the
# structured document tag to treat its contents as text that a user has already entered.
# Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
tag.is_showing_placeholder_text = is_showing_placeholder_text
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlaceholderBuildingBlock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

