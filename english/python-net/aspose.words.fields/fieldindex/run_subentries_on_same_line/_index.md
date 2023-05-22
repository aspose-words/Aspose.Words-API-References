---
title: FieldIndex.run_subentries_on_same_line property
linktitle: run_subentries_on_same_line property
articleTitle: run_subentries_on_same_line property
second_title: Aspose.Words for Python
description: "FieldIndex.run_subentries_on_same_line property. Gets or sets whether run subentries into the same line as the main entry."
type: docs
weight: 140
url: /python-net/aspose.words.fields/fieldindex/run_subentries_on_same_line/
---

## FieldIndex.run_subentries_on_same_line property

Gets or sets whether run subentries into the same line as the main entry.


### Examples

Shows how to work with subentries in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create an INDEX field which will display an entry for each XE field found in the document.
# Each entry will display the XE field's "text" property value on the left side,
# and the number of the page that contains the XE field on the right.
# The INDEX entry will collect all XE fields with matching values in the "text" property
# into one entry as opposed to making an entry for each XE field.
index = builder.insert_field(aw.fields.FieldType.FIELD_INDEX, True).as_field_index()
index.page_number_separator = ", see page "
index.heading = "A"

# XE fields that have a "text" property whose value becomes the heading of the INDEX entry.
# If this value contains two string segments split by a colon (the INDEX entry will treat :) delimiter,
# the first segment is heading, and the second segment will become the subheading.
# The INDEX field first groups entries alphabetically, then, if there are multiple XE fields with the same
# headings, the INDEX field will further subgroup them by the values of these headings.
# There can be multiple subgrouping layers, depending on how many times
# the "text" properties of XE fields get segmented like this.
# By default, an INDEX field entry group will create a new line for every subheading within this group.
# We can set the "run_subentries_on_same_line" flag to "True" to keep the heading,
# and every subheading for the group on one line instead, which will make the INDEX field more compact.
index.run_subentries_on_same_line = run_subentries_on_the_same_line

if run_subentries_on_the_same_line:
    self.assertEqual(" INDEX  \\e \", see page \" \\h A \\r", index.get_field_code())
else:
    self.assertEqual(" INDEX  \\e \", see page \" \\h A", index.get_field_code())

# Insert two XE fields, each on a new page, and with the same heading named "Heading 1",
# which the INDEX field will use to group them.
# If "run_subentries_on_same_line" is "False", then the INDEX table will create three lines:
# one line for the grouping heading "Heading 1", and one more line for each subheading.
# If "run_subentries_on_same_line" is "True", then the INDEX table will create a one-line
# entry that encompasses the heading and every subheading.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Heading 1:Subheading 1"

self.assertEqual(" XE  \"Heading 1:Subheading 1\"", index_entry.get_field_code())

builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = "Heading 1:Subheading 2"

doc.update_page_layout()
doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_index_subheading.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

