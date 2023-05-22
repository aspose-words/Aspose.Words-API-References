---
title: DropDownItemCollection indexer
linktitle: DropDownItemCollection indexer
articleTitle: DropDownItemCollection indexer
second_title: Aspose.Words for Python
description: "DropDownItemCollection indexer. Gets or sets the element at the specified index."
type: docs
weight: 10
url: /python-net/aspose.words.fields/dropdownitemcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets or sets the element at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

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

* module [aspose.words.fields](../../)
* class [DropDownItemCollection](../)

