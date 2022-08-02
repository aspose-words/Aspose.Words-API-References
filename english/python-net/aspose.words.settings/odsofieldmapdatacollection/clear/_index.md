---
title: clear method
second_title: Aspose.Words for Python via .NET API Reference
description: "Removes all elements from this collection."
type: docs
weight: 50
url: /python-net/aspose.words.settings/odsofieldmapdatacollection/clear/
---

## clear() {#default}

Removes all elements from this collection.


```python
def clear(self):
    ...
```

### Examples

Shows how to access the collection of data that maps data source columns to merge fields.

```python
doc = aw.Document(MY_DIR + "Odso data.docx")

# This collection defines how a mail merge will map columns from a data source
# to predefined MERGEFIELD, ADDRESSBLOCK and GREETINGLINE fields.
data_collection = doc.mail_merge_settings.odso.field_map_datas
self.assertEqual(30, data_collection.count)

for index, data in enumerate(data_collection):
    print(f"Field map data index {index}, type \"{data.type}\":")

    if data.type != aw.settings.OdsoFieldMappingType.NULL:
        print(f"\tColumn \"{data.name}\", number {data.column} mapped to merge field \"{data.mapped_name}\".")
    else:
        print("\tNo valid column to field mapping data present.")

# Clone the elements in this collection.
#Assert.are_not_equal(data_collection[0], data_collection[0].clone())

# Use the "remove_at" method elements individually by index.
data_collection.remove_at(0)

self.assertEqual(29, data_collection.count)

# Use the "clear" method to clear the entire collection at once.
data_collection.clear()

self.assertEqual(0, data_collection.count)
```

### See Also

* module [aspose.words.settings](../../)
* class [OdsoFieldMapDataCollection](../)

