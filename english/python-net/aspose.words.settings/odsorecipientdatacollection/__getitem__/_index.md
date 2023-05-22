---
title: OdsoRecipientDataCollection indexer
linktitle: OdsoRecipientDataCollection indexer
articleTitle: OdsoRecipientDataCollection indexer
second_title: Aspose.Words for Python
description: "OdsoRecipientDataCollection indexer. Gets or sets an item in this collection."
type: docs
weight: 20
url: /python-net/aspose.words.settings/odsorecipientdatacollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets or sets an item in this collection.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

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
* class [OdsoRecipientDataCollection](../)

