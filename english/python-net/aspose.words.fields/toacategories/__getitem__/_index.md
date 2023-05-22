---
title: ToaCategories indexer
linktitle: ToaCategories indexer
articleTitle: ToaCategories indexer
second_title: Aspose.Words for Python
description: "ToaCategories indexer. Gets or sets the category heading by category number."
type: docs
weight: 20
url: /python-net/aspose.words.fields/toacategories/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets or sets the category heading by category number.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to specify a set of categories for TOA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# TOA fields can filter their entries by categories defined in this collection.
toa_categories = aw.fields.ToaCategories()
doc.field_options.toa_categories = toa_categories

# This collection of categories comes with default values, which we can overwrite with custom values.
self.assertEqual("Cases", toa_categories[1])
self.assertEqual("Statutes", toa_categories[2])

toa_categories[1] = "My Category 1"
toa_categories[2] = "My Category 2"

# We can always access the default values via this collection.
self.assertEqual("Cases", aw.fields.ToaCategories.default_categories[1])
self.assertEqual("Statutes", aw.fields.ToaCategories.default_categories[2])

# Insert 2 TOA fields. TOA fields create an entry for each TA field in the document.
# Use the "\c" switch to select the index of a category from our collection.
#  With this switch, a TOA field will only pick up entries from TA fields that
# also have a "\c" switch with a matching category index. Each TOA field will also display
# the name of the category that its "\c" switch points to.
builder.insert_field("TOA \\c 1 \\h", None)
builder.insert_field("TOA \\c 2 \\h", None)
builder.insert_break(aw.BreakType.PAGE_BREAK)

# Insert TOA entries across 2 categories. Our first TOA field will receive one entry,
# from the second TA field whose "\c" switch also points to the first category.
# The second TOA field will have two entries from the other two TA fields.
builder.insert_field("TA \\c 2 \\l \"entry 1\"")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field("TA \\c 1 \\l \"entry 2\"")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field("TA \\c 2 \\l \"entry 3\"")

doc.update_fields()
doc.save(ARTIFACTS_DIR + "FieldOptions.table_of_authority_categories.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [ToaCategories](../)

