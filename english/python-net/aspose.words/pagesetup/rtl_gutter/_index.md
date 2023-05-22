---
title: PageSetup.rtl_gutter property
linktitle: rtl_gutter property
articleTitle: rtl_gutter property
second_title: Aspose.Words for Python
description: "PageSetup.rtl_gutter property. Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language."
type: docs
weight: 380
url: /python-net/aspose.words/pagesetup/rtl_gutter/
---

## PageSetup.rtl_gutter property

Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.


### Examples

Shows how to set gutter margins.

```python
doc = aw.Document()

# Insert text that spans several pages.
builder = aw.DocumentBuilder(doc)
for i in range(6):
    builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")
    builder.insert_break(aw.BreakType.PAGE_BREAK)

# A gutter adds whitespaces to either the left or right page margin,
# which makes up for the center folding of pages in a book encroaching on the page's layout.
page_setup = doc.sections[0].page_setup

# Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
self.assertAlmostEqual(470.30, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)

page_setup.gutter = 100.0

# Set the "rtl_gutter" property to "True" to place the gutter in a more suitable position for right-to-left text.
page_setup.rtl_gutter = True

# Set the "multiple_pages" property to "MultiplePagesType.MIRROR_MARGINS" to alternate
# the left/right page side position of margins every page.
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS

doc.save(ARTIFACTS_DIR + "PageSetup.gutter.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

