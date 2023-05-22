---
title: ViewOptions.do_not_display_page_boundaries property
linktitle: do_not_display_page_boundaries property
articleTitle: do_not_display_page_boundaries property
second_title: Aspose.Words for Python
description: "ViewOptions.do_not_display_page_boundaries property. Turns off display of the space between the top of the text and the top edge of the page."
type: docs
weight: 20
url: /python-net/aspose.words.settings/viewoptions/do_not_display_page_boundaries/
---

## ViewOptions.do_not_display_page_boundaries property

Turns off display of the space between the top of the text and the top edge of the page.


### Examples

Shows how to hide vertical whitespace and headers/footers in view options.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert content that spans across 3 pages.
builder.writeln("Paragraph 1, Page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Paragraph 2, Page 2.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Paragraph 3, Page 3.")

# Insert a header and a footer.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln("This is the header.")
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln("This is the footer.")

# This document contains a small amount of content that takes up a few full pages worth of space.
# Set the "do_not_display_page_boundaries" flag to "True" to get older versions of Microsoft Word to omit headers,
# footers, and much of the vertical whitespace when displaying our document.
# Set the "do_not_display_page_boundaries" flag to "False" to get older versions of Microsoft Word
# to normally display our document.
doc.view_options.do_not_display_page_boundaries = do_not_display_page_boundaries

doc.save(ARTIFACTS_DIR + "ViewOptions.display_page_boundaries.doc")
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

