---
title: multiple_pages property
second_title: Aspose.Words for Python via .NET API Reference
description: "For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet."
type: docs
weight: 260
url: /python-net/aspose.words/pagesetup/multiple_pages/
---

## PageSetup.multiple_pages property

For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet.


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

Shows how to configure a document that can be printed as a book fold.

```python
doc = aw.Document()

# Insert text that spans 16 pages.
builder = aw.DocumentBuilder(doc)
builder.writeln("My Booklet:")

for i in range(15):

    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f"Booklet face #{i}")

# Configure the first section's "page_setup" property to print the document in the form of a book fold.
# When we print this document on both sides, we can take the pages to stack them
# and fold them all down the middle at once. The contents of the document will line up into a book fold.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING

# We can only specify the number of sheets in multiples of 4.
page_setup.sheets_per_booklet = 4

doc.save(ARTIFACTS_DIR + "PageSetup.booklet.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

