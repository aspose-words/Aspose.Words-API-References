---
title: sheets_per_booklet property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns or sets the number of pages to be included in each booklet."
type: docs
weight: 390
url: /python-net/aspose.words/pagesetup/sheets_per_booklet/
---

## PageSetup.sheets_per_booklet property

Returns or sets the number of pages to be included in each booklet.


### Examples

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

