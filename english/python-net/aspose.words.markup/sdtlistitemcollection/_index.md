---
title: SdtListItemCollection class
linktitle: SdtListItemCollection class
articleTitle: SdtListItemCollection class
second_title: Aspose.Words for Python
description: "aspose.words.markup.SdtListItemCollection class. Provides access to [SdtListItem](../sdtlistitem/) elements of a structured document tag"
type: docs
weight: 140
url: /python-net/aspose.words.markup/sdtlistitemcollection/
---

## SdtListItemCollection class

Provides access to [SdtListItem](../sdtlistitem/) elements of a structured document tag.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a [SdtListItem](../sdtlistitem/) object given its zero-based index in the collection. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets number of items in the collection. |
| [selected_value](./selected_value/) | Specifies currently selected value in this list. Null value allowed, meaning that no currently selected entry is associated with this list item collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(item)](./add/#sdtlistitem) | Adds an item to this collection. |
|[ clear()](./clear/#default) | Clears all items from this collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a list item at the specified index. |

### Examples

Shows how to work with drop down-list structured document tags.

```python
doc = aw.Document()
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.DROP_DOWN_LIST, aw.markup.MarkupLevel.BLOCK)
doc.first_section.body.append_child(tag)
list_items = tag.list_items
list_items.add(aw.markup.SdtListItem(value='Value 1'))
assert list_items[0].display_text == list_items[0].value
list_items.add(aw.markup.SdtListItem(display_text='Item 2', value='Value 2'))
list_items.add(aw.markup.SdtListItem(display_text='Item 3', value='Value 3'))
list_items.add(aw.markup.SdtListItem(display_text='Item 4', value='Value 4'))
assert list_items.count == 4
list_items.selected_value = list_items[3]
assert list_items.selected_value.value == 'Value 4'
for item in list_items:
    if item is not None:
        print(f'List item: {item.display_text}, value: {item.value}')
list_items.remove_at(3)
assert list_items.count == 3
list_items.selected_value = list_items[1]
doc.save(ARTIFACTS_DIR + 'StructuredDocumentTag.ListItemCollection.docx')
list_items.clear()
assert list_items.count == 0
```

### See Also

* module [aspose.words.markup](../)

