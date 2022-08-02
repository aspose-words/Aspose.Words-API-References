---
title: active property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether the record from the data source shall be imported into a document when the mail merge is performed"
type: docs
weight: 20
url: /python-net/aspose.words.settings/odsorecipientdata/active/
---

## OdsoRecipientData.active property

Specifies whether the record from the data source shall be imported into a document when the mail merge is performed.
The default value is ``true``.



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

* module [aspose.words.settings](../../)
* class [OdsoRecipientData](../)

