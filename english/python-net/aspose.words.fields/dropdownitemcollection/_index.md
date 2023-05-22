﻿---
title: DropDownItemCollection class
linktitle: DropDownItemCollection class
articleTitle: DropDownItemCollection class
second_title: Aspose.Words for Python
description: "aspose.words.fields.DropDownItemCollection class. A collection of strings that represent all the items in a drop-down form field"
type: docs
weight: 40
url: /python-net/aspose.words.fields/dropdownitemcollection/
---

## DropDownItemCollection class

A collection of strings that represent all the items in a drop-down form field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets the element at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(value)](./add/#str) | Adds a string to the end of the collection. |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ contains(value)](./contains/#str) | Determines whether the collection contains the specified value. |
|[ index_of(value)](./index_of/#str) | Returns the zero-based index of the specified value in the collection. |
|[ insert(index, value)](./insert/#int_str) | Inserts a string into the collection at the specified index. |
|[ remove(name)](./remove/#str) | Removes the specified value from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a value at the specified index. |

### Examples

Shows how to insert a combo box field, and edit the elements in its item collection.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a combo box, and then verify its collection of drop-down items.
# In Microsoft Word, the user will click the combo box,
# and then choose one of the items of text in the collection to display.
items = ["One", "Two", "Three"]
combo_box_field = builder.insert_combo_box("DropDown", items, 0)
drop_down_items = combo_box_field.drop_down_items

self.assertEqual(3, drop_down_items.count)
self.assertEqual("One", drop_down_items[0])
self.assertEqual(1, drop_down_items.index_of("Two"))
self.assertTrue(drop_down_items.contains("Three"))

# There are two ways of adding a new item to an existing collection of drop-down box items.
# 1 -  Append an item to the end of the collection:
drop_down_items.add("Four")

# 2 -  Insert an item before another item at a specified index:
drop_down_items.insert(3, "Three and a half")

self.assertEqual(5, drop_down_items.count)

# Iterate over the collection and print every element.
for drop_down in drop_down_items:
    print(drop_down)

# There are two ways of removing elements from a collection of drop-down items.
# 1 -  Remove an item with contents equal to the passed string:
drop_down_items.remove("Four")

# 2 -  Remove an item at an index:
drop_down_items.remove_at(3)

self.assertEqual(3, drop_down_items.count)
self.assertFalse(drop_down_items.contains("Three and a half"))
self.assertFalse(drop_down_items.contains("Four"))

doc.save(ARTIFACTS_DIR + "FormFields.drop_down_item_collection.html")

# Empty the whole collection of drop-down items.
drop_down_items.clear()
```

### See Also

* module [aspose.words.fields](../)
* class [FormField](../formfield/)
* property [FormField.drop_down_items](../formfield/drop_down_items/)

