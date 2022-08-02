---
title: paper_size property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns or sets the paper size."
type: docs
weight: 340
url: /python-net/aspose.words/pagesetup/paper_size/
---

## PageSetup.paper_size property

Returns or sets the paper size.

Setting this property updates [PageSetup.page_width](../page_width/) and [PageSetup.page_height](../page_height/) values.
Setting this value to [PaperSize.CUSTOM](../../papersize/#CUSTOM) does not change existing values.




### Examples

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

Shows how to set page sizes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# We can change the current page's size to a pre-defined size
# by using the "paper_size" property of this section's PageSetup object.
builder.page_setup.paper_size = aw.PaperSize.TABLOID

self.assertEqual(792.0, builder.page_setup.page_width)
self.assertEqual(1224.0, builder.page_setup.page_height)

builder.writeln(f"This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.")

# Each section has its own PageSetup object. When we use a document builder to make a new section,
# that section's PageSetup object inherits all the previous section's PageSetup object's values.
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)

self.assertEqual(aw.PaperSize.TABLOID, builder.page_setup.paper_size)

builder.page_setup.paper_size = aw.PaperSize.A5
builder.writeln(f"This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.")

self.assertEqual(419.55, builder.page_setup.page_width)
self.assertEqual(595.30, builder.page_setup.page_height)

builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)

# Set a custom size for this section's pages.
builder.page_setup.page_width = 620
builder.page_setup.page_height = 480

self.assertEqual(aw.PaperSize.CUSTOM, builder.page_setup.paper_size)

builder.writeln(f"This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.")

doc.save(ARTIFACTS_DIR + "PageSetup.paper_sizes.docx")
```

Shows how to construct an Aspose.Words document by hand.

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

# Set some page setup properties for the section.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER

# A section needs a body, which will contain and display all its contents
# on the page between the section's header and footer.
body = aw.Body(doc)
section.append_child(body)

# Create a paragraph, set some formatting properties, and then append it as a child to the body.
para = aw.Paragraph(doc)

para.paragraph_format.style_name = "Heading 1"
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER

body.append_child(para)

# Finally, add some content to do the document. Create a run,
# set its appearance and contents, and then append it as a child to the paragraph.
run = aw.Run(doc)
run.text = "Hello World!"
run.font.color = drawing.Color.red
para.append_child(run)

self.assertEqual("Hello World!", doc.get_text().strip())

doc.save(ARTIFACTS_DIR + "Section.create_manually.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

