---
title: hash property
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents the hash code for this record"
type: docs
weight: 40
url: /python-net/aspose.words.settings/odsorecipientdata/hash/
---

## OdsoRecipientData.hash property

Represents the hash code for this record. 
Sometimes Microsoft Word uses [OdsoRecipientData.hash](./) of a whole record instead of a [OdsoRecipientData.unique_tag](../unique_tag/) value.
The default value is 0.



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

