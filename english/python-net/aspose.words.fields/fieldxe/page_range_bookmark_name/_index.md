---
title: FieldXE.page_range_bookmark_name property
linktitle: page_range_bookmark_name property
articleTitle: page_range_bookmark_name property
second_title: Aspose.Words for Python
description: "FieldXE.page_range_bookmark_name property. Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number."
type: docs
weight: 60
url: /python-net/aspose.words.fields/fieldxe/page_range_bookmark_name/
---

## FieldXE.page_range_bookmark_name property

Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number.


### Examples

Shows how to specify a bookmark's spanned pages as a page range for an INDEX field entry.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create an INDEX field which will display an entry for each XE field found in the document.
# Each entry will display the XE field's "text" property value on the left side,
# and the number of the page that contains the XE field on the right.
# The INDEX entry will collect all XE fields with matching values in the "text" property
# into one entry as opposed to making an entry for each XE field.
index = builder.insert_field(aw.fields.FieldType.FIELD_INDEX, True).as_field_index()

# For INDEX entries that display page ranges, we can specify a separator string
# which will appear between the number of the first page, and the number of the last.
index.page_number_separator = ", on page(s) "
index.page_range_separator = " to "

self.assertEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.get_field_code())

builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "My entry"

# If an XE field names a bookmark using the page_range_bookmark_name property,
# its INDEX entry will show the range of pages that the bookmark spans
# instead of the number of the page that contains the XE field.
index_entry.page_range_bookmark_name = "MyBookmark"

self.assertEqual(" XE  \"My entry\" \\r MyBookmark", index_entry.get_field_code())
self.assertEqual("MyBookmark", index_entry.page_range_bookmark_name)

# Insert a bookmark that starts on page 3 and ends on page 5.
# The INDEX entry for the XE field that references this bookmark will display this page range.
# In our table, the INDEX entry will display "My entry, on page(s) 3 to 5".
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark("MyBookmark")
builder.write("Start of MyBookmark")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write("End of MyBookmark")
builder.end_bookmark("MyBookmark")

doc.update_page_layout()
doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_index_page_range_bookmark.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

