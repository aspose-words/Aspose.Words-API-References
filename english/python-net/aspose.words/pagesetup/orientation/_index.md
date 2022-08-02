---
title: orientation property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns or sets the orientation of the page."
type: docs
weight: 280
url: /python-net/aspose.words/pagesetup/orientation/
---

## PageSetup.orientation property

Returns or sets the orientation of the page.

Changing **Orientation** swaps [PageSetup.page_width](../page_width/) and [PageSetup.page_height](../page_height/).




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

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.page_setup.paper_size = aw.PaperSize.LEGAL
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.top_margin = aw.ConvertUtil.inch_to_point(1.0)
builder.page_setup.bottom_margin = aw.ConvertUtil.inch_to_point(1.0)
builder.page_setup.left_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.right_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.header_distance = aw.ConvertUtil.inch_to_point(0.2)
builder.page_setup.footer_distance = aw.ConvertUtil.inch_to_point(0.2)

builder.writeln("Hello world!")

doc.save(ARTIFACTS_DIR + "PageSetup.page_margins.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

