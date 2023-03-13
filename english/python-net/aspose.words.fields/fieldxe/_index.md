﻿---
title: FieldXE class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the XE field"
type: docs
weight: 1150
url: /python-net/aspose.words.fields/fieldxe/
---

## FieldXE class

Implements the XE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Defines the text and page number for an index entry, which is used by an INDEX field.


**Inheritance:** [FieldXE](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldXE()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_type](./entry_type/) | Gets or sets an index entry type. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_bold](./is_bold/) | Gets or sets whether to apply bold formatting to the entry's page number. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_italic](./is_italic/) | Gets or sets whether to apply italic formatting to the entry's page number. |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [page_number_replacement](./page_number_replacement/) | Gets or sets text used in place of a page number. |
| [page_range_bookmark_name](./page_range_bookmark_name/) | Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [text](./text/) | Gets or sets the text of the entry. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [yomi](./yomi/) | Gets or sets the yomi (first phonetic character for sorting indexes) for the index entry |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

doc.update_page_layout()
doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_index_filter.docx")
```

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create an INDEX field which will display an entry for each XE field found in the document.
# Each entry will display the XE field's Text property value on the left side,
# and the number of the page that contains the XE field on the right.
# If the XE fields have the same value in their "text" property,
# the INDEX field will group them into one entry.
index = builder.insert_field(aw.fields.FieldType.FIELD_INDEX, True).as_field_index()
index.language_id = "1033" # en-US

# Setting this property's value to "A" will group all the entries by their first letter,
# and place that letter in uppercase above each group.
index.heading = "A"

# Set the table created by the INDEX field to span over 2 columns.
index.number_of_columns = "2"

# Set any entries with starting letters outside the "a-c" character range to be omitted.
index.letter_range = "a-c"

self.assertEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.get_field_code())

# These next two XE fields will show up under the "A" heading,
# with their respective text stylings also applied to their page numbers.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Apple"
index_entry.is_italic = True

self.assertEqual(" XE  Apple \\i", index_entry.get_field_code())

builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Apricot"
index_entry.is_bold = True

self.assertEqual(" XE  Apricot \\b", index_entry.get_field_code())

# Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Banana"

builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Cherry"

# INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Avocado"

# This entry will not appear because it starts with the letter "D",
# which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Durian"

doc.update_page_layout()
doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_index_formatting.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

