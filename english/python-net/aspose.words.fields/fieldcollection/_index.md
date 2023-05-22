﻿---
title: FieldCollection class
linktitle: FieldCollection class
articleTitle: FieldCollection class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldCollection class. A collection of [Field](../field/) objects that represents the fields in the specified range"
type: docs
weight: 230
url: /python-net/aspose.words.fields/fieldcollection/
---

## FieldCollection class

A collection of [Field](../field/) objects that represents the fields in the specified range.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




An instance of this collection iterates fields which start fall within the specified range.

The [FieldCollection](./) collection does not own the fields it contains, rather, is just a selection of fields.

The [FieldCollection](./) collection is "live", i.e. changes to the children of the node object
that it was created from are immediately reflected in the fields returned by the [FieldCollection](./)
properties and methods.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a field at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of the fields in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Removes all fields of this collection from the document and from this collection itself. |
|[ remove(field)](./remove/#field) | Removes the specified field from this collection and from the document. |
|[ remove_at(index)](./remove_at/#int) | Removes a field at the specified index from this collection and from the document. |

### Examples

Shows how to remove fields from a field collection.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_field(" DATE \\@ \"dddd, d MMMM yyyy\" ")
builder.insert_field(" TIME ")
builder.insert_field(" REVNUM ")
builder.insert_field(" AUTHOR  \"John Doe\" ")
builder.insert_field(" SUBJECT \"My Subject\" ")
builder.insert_field(" QUOTE \"Hello world!\" ")
doc.update_fields()

fields = doc.range.fields

self.assertEqual(6, fields.count)

# Below are four ways of removing fields from a field collection.
# 1 -  Get a field to remove itself:
fields[0].remove()
self.assertEqual(5, fields.count)

# 2 -  Get the collection to remove a field that we pass to its removal method:
last_field = fields[3]
fields.remove(last_field)
self.assertEqual(4, fields.count)

# 3 -  Remove a field from a collection at an index:
fields.remove_at(2)
self.assertEqual(3, fields.count)

# 4 -  Remove all the fields from the collection at once:
fields.clear()
self.assertEqual(0, fields.count)
```

### See Also

* module [aspose.words.fields](../)

