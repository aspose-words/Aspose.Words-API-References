---
title: DocumentBuilder.page_setup property
linktitle: page_setup property
articleTitle: page_setup property
second_title: Aspose.Words for Python
description: "DocumentBuilder.page_setup property. Returns an object that represents current page setup and section properties."
type: docs
weight: 160
url: /python-net/aspose.words/documentbuilder/page_setup/
---

## DocumentBuilder.page_setup property

Returns an object that represents current page setup and section properties.


### Examples

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Modify the page setup properties for the builder's current section and add text.
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln("This is the first section, which landscape oriented with vertically centered text.")

# If we start a new section using a document builder,
# it will inherit the builder's current page setup properties.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)

self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)

# We can revert its page setup properties to their default values using the "ClearFormatting" method.
builder.page_setup.clear_formatting()

self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)

builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.")

doc.save(ARTIFACTS_DIR + "PageSetup.clear_formatting.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

