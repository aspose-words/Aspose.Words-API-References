---
title: FieldIndex.number_of_columns property
linktitle: number_of_columns property
articleTitle: number_of_columns property
second_title: Aspose.Words for Python
description: "FieldIndex.number_of_columns property. Gets or sets the number of columns per page used when building the index."
type: docs
weight: 100
url: /python-net/aspose.words.fields/fieldindex/number_of_columns/
---

## FieldIndex.number_of_columns property

Gets or sets the number of columns per page used when building the index.


```python
@property
def number_of_columns(self) -> str:
    ...

@number_of_columns.setter
def number_of_columns(self, value: str):
    ...

```

### Examples

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

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

