---
title: OdsoRecipientDataCollection class
second_title: Aspose.Words for Python via .NET API Reference
description: "A typed collection of [OdsoRecipientData](../odsorecipientdata/)To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article."
type: docs
weight: 170
url: /python-net/aspose.words.settings/odsorecipientdatacollection/
---

## OdsoRecipientDataCollection class

A typed collection of [OdsoRecipientData](../odsorecipientdata/)To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/python-net/mail-merge-and-reporting/) documentation article.







### Constructors
| Name | Description |
| --- | --- |
| [OdsoRecipientDataCollection()](./__init__/#default) | The default constructor. |

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets an item in this collection. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(value)](./add/#odsorecipientdata) | Adds an object to the end of this collection. |
|[ clear()](./clear/#default) | Removes all elements from this collection. |
|[ remove_at(index)](./remove_at/#int) | Removes the element at the specified index. |

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
* class [OdsoRecipientData](../odsorecipientdata/)
* property [Odso.recipient_datas](../odso/recipient_datas/)

