---
title: OdsoRecipientData class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents information about a single record within an external data source that is to be excluded from the mail merge"
type: docs
weight: 160
url: /python-net/aspose.words.settings/odsorecipientdata/
---

## OdsoRecipientData class

Represents information about a single record within an external data source that is to be excluded from the mail merge.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article.




If a record shall be merged into a merged document, then no information is needed about that record. 
However, if a given record shall not be merged into a merged document, then the value of the unique key 
for that record shall be stored in the [OdsoRecipientData.unique_tag](./unique_tag/) property of this object to indicate this exclusion.




### Constructors
| Name | Description |
| --- | --- |
| [OdsoRecipientData()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [active](./active/) | Specifies whether the record from the data source shall be imported into a document when the mail merge is performed. The default value is ``True``. |
| [column](./column/) | Specifies the column within the data source that contains unique data for the current record. The default value is 0. |
| [hash](./hash/) | Represents the hash code for this record.  Sometimes Microsoft Word uses [OdsoRecipientData.hash](./hash/) of a whole record instead of a [OdsoRecipientData.unique_tag](./unique_tag/) value. The default value is 0. |
| [unique_tag](./unique_tag/) | Specifies the contents of a given record in the column containing unique data. The default value is ``None``. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Returns a deep clone of this object. |

### Examples

Shows how to access the collection of data that designates which merge data source records a mail merge will exclude.

```python
doc = aw.Document(MY_DIR + "Odso data.docx")

data_collection = doc.mail_merge_settings.odso.recipient_datas

self.assertEqual(70, data_collection.count)

for index, data in enumerate(data_collection):
    print(f'Odso recipient data index {index} will {"" if data.active else "not "}be imported upon mail merge.')
    print(f"\tColumn #{data.column}")
    print(f"\tHash code: {data.hash}")
    print(f"\tContents array length: {data.unique_tag.length}")

# We can clone the elements in this collection.
self.assertNotEqual(data_collection[0], data_collection[0].clone())

# We can also remove elements individually, or clear the entire collection at once.
data_collection.remove_at(0)

self.assertEqual(69, data_collection.count)

data_collection.clear()

self.assertEqual(0, data_collection.count)
```

### See Also

* module [aspose.words.settings](../)

