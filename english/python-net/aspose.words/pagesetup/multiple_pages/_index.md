﻿---
title: PageSetup.multiple_pages property
linktitle: multiple_pages property
articleTitle: multiple_pages property
second_title: Aspose.Words for Python
description: "PageSetup.multiple_pages property. For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet."
type: docs
weight: 270
url: /python-net/aspose.words/pagesetup/multiple_pages/
---

## PageSetup.multiple_pages property

For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet.


```python
@property
def multiple_pages(self) -> aspose.words.settings.MultiplePagesType:
    ...

@multiple_pages.setter
def multiple_pages(self, value: aspose.words.settings.MultiplePagesType):
    ...

```

### Examples

Shows how to set gutter margins.

```python
doc = aw.Document()
# Insert text that spans several pages.
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 6:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# A gutter adds whitespaces to either the left or right page margin,
# which makes up for the center folding of pages in a book encroaching on the page's layout.
page_setup = doc.sections[0].page_setup
# Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
self.assertAlmostEqual(470.3, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)
page_setup.gutter = 100
# Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
page_setup.rtl_gutter = True
# Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
# the left/right page side position of margins every page.
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Gutter.docx')
```

Shows how to configure a document that can be printed as a book fold.

```python
doc = aw.Document()
# Insert text that spans 16 pages.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# Configure the first section's "PageSetup" property to print the document in the form of a book fold.
# When we print this document on both sides, we can take the pages to stack them
# and fold them all down the middle at once. The contents of the document will line up into a book fold.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# We can only specify the number of sheets in multiples of 4.
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

