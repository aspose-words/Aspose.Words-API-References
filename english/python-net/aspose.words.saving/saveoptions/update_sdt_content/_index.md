---
title: update_sdt_content property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets value determining whether content of [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) is updated before saving."
type: docs
weight: 170
url: /python-net/aspose.words.saving/saveoptions/update_sdt_content/
---

## SaveOptions.update_sdt_content property

Gets or sets value determining whether content of [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) is updated before saving.


The default value is ``False``.



### Examples

Shows how to update structured document tags while saving a document to PDF.

```python
doc = aw.Document()

# Insert a drop-down list structured document tag.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.DROP_DOWN_LIST, aw.markup.MarkupLevel.BLOCK)
tag.list_items.add(aw.markup.SdtListItem("Value 1"))
tag.list_items.add(aw.markup.SdtListItem("Value 2"))
tag.list_items.add(aw.markup.SdtListItem("Value 3"))

# The drop-down list currently displays "Choose an item" as the default text.
# Set the "selected_value" property to one of the list items to get the tag to
# display that list item's value instead of the default text.
tag.list_items.selected_value = tag.list_items[1]

doc.first_section.body.append_child(tag)

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.update_sdt_content.pdf")
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

