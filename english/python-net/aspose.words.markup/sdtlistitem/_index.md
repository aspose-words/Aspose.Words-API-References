---
title: SdtListItem class
linktitle: SdtListItem class
articleTitle: SdtListItem class
second_title: Aspose.Words for Python
description: "aspose.words.markup.SdtListItem class. This element specifies a single list item within a parent [SdtType.COMBO_BOX](../sdttype/#COMBO_BOX) or [SdtType.DROP_DOWN_LIST](../sdttype/#DROP_DOWN_LIST) structured document tag"
type: docs
weight: 130
url: /python-net/aspose.words.markup/sdtlistitem/
---

## SdtListItem class

This element specifies a single list item within a parent [SdtType.COMBO_BOX](../sdttype/#COMBO_BOX) or [SdtType.DROP_DOWN_LIST](../sdttype/#DROP_DOWN_LIST) structured document tag.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [SdtListItem(display_text, value)](./__init__/#str_str) | Initializes a new instance of this class. |
| [SdtListItem(value)](./__init__/#str) | Initializes a new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [display_text](./display_text/) | Gets the text to display in the run content in place of the [SdtListItem.value](./value/) attribute contents for this list item. |
| [value](./value/) | Gets the value of this list item. |

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

