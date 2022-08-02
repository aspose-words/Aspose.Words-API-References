---
title: get_effective_value method
second_title: Aspose.Words for Python via .NET API Reference
description: "Reports the string representation of the [ListLevel](../) object for the specified index of the list item"
type: docs
weight: 180
url: /python-net/aspose.words.lists/listlevel/get_effective_value/
---

## get_effective_value(index, number_style, custom_number_style_format) {#int_numberstyle_str}

Reports the string representation of the [ListLevel](../) object for the specified index
of the list item. Parameters specify the [NumberStyle](../../../aspose.words/numberstyle/) and an optional format string
used when [NumberStyle.CUSTOM](../../../aspose.words/numberstyle/#CUSTOM) is specified.



```python
def get_effective_value(self, index: int, number_style: aspose.words.NumberStyle, custom_number_style_format: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| number_style | [NumberStyle](../../../aspose.words/numberstyle/) |  |
| custom_number_style_format | str |  |

### Returns

The string representation of the [ListLevel](../) object, described by the numberStyle parameter and
the customNumberStyleFormat parameter, in the list item at the position determined by the index parameter.



### Exceptions

| exception | condition |
| --- | --- |
| System.ArgumentException | customNumberStyleFormat is null or empty when the numberStyle is custom.-or- customNumberStyleFormat is not null or empty when the numberStyle is non-custom.-or- customNumberStyleFormat is invalid. |
| System.ArgumentOutOfRangeException | index is out of range. |

### Examples

Shows how to get the format for a list with the custom number style.

```python
doc = aw.Document(MY_DIR + "List with leading zero.docx")

list_level = doc.first_section.body.paragraphs[0].list_format.list_level

custom_number_style_format = ""

if list_level.number_style == aw.NumberStyle.CUSTOM:
    custom_number_style_format = list_level.custom_number_style_format

self.assertEqual("001, 002, 003, ...", custom_number_style_format)

# We can get value for the specified index of the list item.
self.assertEqual("iv", list_level.get_effective_value(4, aw.NumberStyle.LOWERCASE_ROMAN, None))
self.assertEqual("005", list_level.get_effective_value(5, aw.NumberStyle.CUSTOM, custom_number_style_format))
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

