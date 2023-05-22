---
title: FixedPageSaveOptions.page_set property
linktitle: page_set property
articleTitle: page_set property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.page_set property. Gets or sets the pages to render"
type: docs
weight: 70
url: /python-net/aspose.words.saving/fixedpagesaveoptions/page_set/
---

## FixedPageSaveOptions.page_set property

Gets or sets the pages to render.
Default is all the pages in the document.


### Examples

Shows how to convert only some of the pages in a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 2.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 3.")

with open(ARTIFACTS_DIR + "PdfSaveOptions.one_page.pdf", "wb") as stream:

    # Create a "PdfSaveOptions" object that we can pass to the document's "save" method
    # to modify how that method converts the document to .PDF.
    options = aw.saving.PdfSaveOptions()

    # Set the "page_index" to "1" to render a portion of the document starting from the second page.
    options.page_set = aw.saving.PageSet(1)

    # This document will contain one page starting from page two, which will only contain the second page.
    doc.save(stream, options)
```

Shows how to export Odd pages from the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

for i in range(5):
    builder.writeln("Page " + str(i + 1) + "(" + ("odd" if i % 2 == 0 else "even") + ")")
    if i < 4:
        builder.insert_break(aw.BreakType.PAGE_BREAK)

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Below are three "page_set" properties that we can use to filter out a set of pages from
# our document to save in an output PDF document based on the parity of their page numbers.
# 1 -  Save only the even-numbered pages:
options.page_set = aw.saving.PageSet.even

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.export_page_set.even.pdf", options)

# 2 -  Save only the odd-numbered pages:
options.page_set = aw.saving.PageSet.odd

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.export_page_set.odd.pdf", options)

# 3 -  Save every page:
options.page_set = aw.saving.PageSet.all

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.export_page_set.all.pdf", options)
```

Shows how to extract pages based on exact page indices.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add five pages to the document.
for i in range(1, 6):
    builder.write("Page " + str(i))
    builder.insert_break(aw.BreakType.PAGE_BREAK)

# Create an "XpsSaveOptions" object, which we can pass to the document's "save" method
# to modify how that method converts the document to .XPS.
xps_options = aw.saving.XpsSaveOptions()

# Use the "page_set" property to select a set of the document's pages to save to output XPS.
# In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
xps_options.page_set = aw.saving.PageSet([0, 1, 3])

doc.save(ARTIFACTS_DIR + "XpsSaveOptions.export_exact_pages.xps", xps_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

