---
title: SdtListItemCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "SdtListItemCollection.count property. Gets number of items in the collection."
type: docs
weight: 20
url: /python-net/aspose.words.markup/sdtlistitemcollection/count/
---

## SdtListItemCollection.count property

Gets number of items in the collection.


### Examples

Shows how to work with drop down-list structured document tags.

```python
doc = aw.Document()
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.DROP_DOWN_LIST, aw.markup.MarkupLevel.BLOCK)
doc.first_section.body.append_child(tag)

# A drop-down list structured document tag is a form that allows the user to
# select an option from a list by left-clicking and opening the form in Microsoft Word.
# The "list_items" property contains all list items, and each list item is an "SdtListItem".
list_items = tag.list_items
list_items.add(aw.markup.SdtListItem("Value 1"))

self.assertEqual(list_items[0].display_text, list_items[0].value)

# Add 3 more list items. Initialize these items using a different constructor to the first item
# to display strings that are different from their values.
list_items.add(aw.markup.SdtListItem("Item 2", "Value 2"))
list_items.add(aw.markup.SdtListItem("Item 3", "Value 3"))
list_items.add(aw.markup.SdtListItem("Item 4", "Value 4"))

self.assertEqual(4, list_items.count)

# The drop-down list is displaying the first item. Assign a different list item to the "selected_value" to display it.
list_items.selected_value = list_items[3]

self.assertEqual("Value 4", list_items.selected_value.value)

# Enumerate over the collection and print each element.
for item in list_items:
    if item is not None:
        print(f"List item: {item.display_text}, value: {item.value}")

# Remove the last list item.
list_items.remove_at(3)

self.assertEqual(3, list_items.count)

# Since our drop-down control is set to display the removed item by default, give it an item to display which exists.
list_items.selected_value = list_items[1]

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.list_item_collection.docx")

# Use the "clear" method to empty the entire drop-down item collection at once.
list_items.clear()

self.assertEqual(0, list_items.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [SdtListItemCollection](../)

