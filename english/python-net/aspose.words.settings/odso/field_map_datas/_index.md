---
title: Odso.field_map_datas property
linktitle: field_map_datas property
articleTitle: field_map_datas property
second_title: Aspose.Words for Python
description: "Odso.field_map_datas property. Gets or sets a collection of objects that specify how columns from the external data source  are mapped to the predefined merge field names in the document"
type: docs
weight: 50
url: /python-net/aspose.words.settings/odso/field_map_datas/
---

## Odso.field_map_datas property

Gets or sets a collection of objects that specify how columns from the external data source 
are mapped to the predefined merge field names in the document.
This object is never ``None``.



```python
@property
def field_map_datas(self) -> aspose.words.settings.OdsoFieldMapDataCollection:
    ...

@field_map_datas.setter
def field_map_datas(self, value: aspose.words.settings.OdsoFieldMapDataCollection):
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
* class [Odso](../)

