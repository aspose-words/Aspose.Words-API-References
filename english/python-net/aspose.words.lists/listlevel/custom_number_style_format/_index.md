---
title: ListLevel.custom_number_style_format property
linktitle: custom_number_style_format property
articleTitle: custom_number_style_format property
second_title: Aspose.Words for Python
description: "ListLevel.custom_number_style_format property. Gets or sets the custom number style format for this list level"
type: docs
weight: 20
url: /python-net/aspose.words.lists/listlevel/custom_number_style_format/
---

## ListLevel.custom_number_style_format property

Gets or sets the custom number style format for this list level. For example: "a, ç, ĝ, ...".


```python
@property
def custom_number_style_format(self) -> str:
    ...

@custom_number_style_format.setter
def custom_number_style_format(self, value: str):
    ...

```

### Examples

Shows how to get the format for a list with the custom number style.

```python
doc = aw.Document(file_name=MY_DIR + 'List with leading zero.docx')
list_level = doc.first_section.body.paragraphs[0].list_format.list_level
custom_number_style_format = ''
if list_level.number_style == aw.NumberStyle.CUSTOM:
    custom_number_style_format = list_level.custom_number_style_format
self.assertEqual('001, 002, 003, ...', custom_number_style_format)
# We can get value for the specified index of the list item.
self.assertEqual('iv', aw.lists.ListLevel.get_effective_value(4, aw.NumberStyle.LOWERCASE_ROMAN, None))
self.assertEqual('005', aw.lists.ListLevel.get_effective_value(5, aw.NumberStyle.CUSTOM, custom_number_style_format))
```

Shows how to set customer number style format.

```python
doc = aw.Document(file_name=MY_DIR + 'List with leading zero.docx')
doc.update_list_labels()
paras = doc.first_section.body.paragraphs
self.assertEqual('001.', paras[0].list_label.label_string)
self.assertEqual('0001.', paras[1].list_label.label_string)
self.assertEqual('0002.', paras[2].list_label.label_string)
paras[1].list_format.list_level.custom_number_style_format = '001, 002, 003, ...'
doc.update_list_labels()
self.assertEqual('001.', paras[0].list_label.label_string)
self.assertEqual('001.', paras[1].list_label.label_string)
self.assertEqual('002.', paras[2].list_label.label_string)
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

