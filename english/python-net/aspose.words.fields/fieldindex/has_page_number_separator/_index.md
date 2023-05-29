---
title: FieldIndex.has_page_number_separator property
linktitle: has_page_number_separator property
articleTitle: has_page_number_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.has_page_number_separator property. Gets a value indicating whether a page number separator is overridden through the field's code."
type: docs
weight: 50
url: /python-net/aspose.words.fields/fieldindex/has_page_number_separator/
---

## FieldIndex.has_page_number_separator property

Gets a value indicating whether a page number separator is overridden through the field's code.


### Examples

Shows how to edit the page number separator in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create an INDEX field which will display an entry for each XE field found in the document.
# Each entry will display the XE field's "text" property value on the left side,
# and the number of the page that contains the XE field on the right.
# The INDEX entry will group XE fields with matching values in the "text" property
# into one entry as opposed to making an entry for each XE field.
index = builder.insert_field(aw.fields.FieldType.FIELD_INDEX, True).as_field_index()

# If our INDEX field has an entry for a group of XE fields,
# this entry will display the number of each page that contains an XE field that belongs to this group.
# We can set custom separators to customize the appearance of these page numbers.
index.page_number_separator = ", on page(s) "
index.page_number_list_separator = " & "

self.assertEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.get_field_code())
self.assertTrue(index.has_page_number_separator)

# After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "First entry"

self.assertEqual(" XE  \"First entry\"", index_entry.get_field_code())

builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "First entry"

builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "First entry"

doc.update_page_layout()
doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_index_page_number_separator.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

