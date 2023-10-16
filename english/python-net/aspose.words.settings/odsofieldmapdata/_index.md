---
title: OdsoFieldMapData class
linktitle: OdsoFieldMapData class
articleTitle: OdsoFieldMapData class
second_title: Aspose.Words for Python
description: "aspose.words.settings.OdsoFieldMapData class. Specifies how a column in the external data source shall be mapped to the predefined merge fields within the document"
type: docs
weight: 140
url: /python-net/aspose.words.settings/odsofieldmapdata/
---

## OdsoFieldMapData class

Specifies how a column in the external data source shall be mapped to the predefined merge fields within the document.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article.




Microsoft Word provides some predefined merge field names that it allows to insert into a document as MERGEFIELD or 
use in the ADDRESSBLOCK or GREETINGLINE fields. The information specified in [OdsoFieldMapData](./)
allows to map one column in the external data source to a single predefined merge field.




### Constructors
| Name | Description |
| --- | --- |
| [OdsoFieldMapData()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [column](./column/) | Specifies the zero-based index of the column within an external data source which shall be mapped to the local name of a specific MERGEFIELD field. The default value is 0. |
| [mapped_name](./mapped_name/) | Specifies the predefined merge field name which shall be mapped to the column number  specified by the [OdsoFieldMapData.column](./column/) property within this field mapping. The default value is an empty string. |
| [name](./name/) | Specifies the column name within an external data source for the column whose  index is specified by the [OdsoFieldMapData.column](./column/) property. The default value is an empty string. |
| [type](./type/) | Specifies if a given mail merge field has been mapped to a column in the given external data source or not. The default value is [OdsoFieldMappingType.DEFAULT](../odsofieldmappingtype/#DEFAULT). |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Returns a deep clone of this object. |

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

* module [aspose.words.settings](../)
* class [OdsoFieldMapDataCollection](../odsofieldmapdatacollection/)
* class [Odso](../odso/)

