﻿---
title: bookmark_name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the name of the bookmark that marks the portion of the document used to build the index."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldindex/bookmark_name/
---

## FieldIndex.bookmark_name property

Gets or sets the name of the bookmark that marks the portion of the document used to build the index.


### Examples

Shows how to create an INDEX field, and then use XE fields to populate it with entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create an INDEX field which will display an entry for each XE field found in the document.
# Each entry will display the XE field's Text property value on the left side
# and the page containing the XE field on the right.
# If the XE fields have the same value in their "text" property,
# the INDEX field will group them into one entry.
index = builder.insert_field(aw.fields.FieldType.FIELD_INDEX, True).as_field_index()

# Configure the INDEX field only to display XE fields that are within the bounds
# of a bookmark named "MainBookmark", and whose "entry_type" properties have a value of "A".
# For both INDEX and XE fields, the "entry_type" property only uses the first character of its string value.
index.bookmark_name = "MainBookmark"
index.entry_type = "A"

self.assertEqual(" INDEX  \\b MainBookmark \\f A", index.get_field_code())

# On a new page, start the bookmark with a name that matches the value
# of the INDEX field's "bookmark_name" property.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark("MainBookmark")

# The INDEX field will pick up this entry because it is inside the bookmark,
# and its entry type also matches the INDEX field's entry type.
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Index entry 1"
index_entry.entry_type = "A"

self.assertEqual(" XE  \"Index entry 1\" \\f A", index_entry.get_field_code())

# Insert an XE field that will not appear in the INDEX because the entry types do not match.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Index entry 2"
index_entry.entry_type = "B"

# End the bookmark and insert an XE field afterwards.
# It is of the same type as the INDEX field, but will not appear
# since it is outside the bookmark's boundaries.
builder.end_bookmark("MainBookmark")
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Index entry 3"
index_entry.entry_type = "A"

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_index_filter.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)
