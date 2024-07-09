---
title: ListLevel.get_effective_value method
linktitle: get_effective_value method
articleTitle: get_effective_value method
second_title: Aspose.Words for Python
description: "ListLevel.get_effective_value method. Reports the string representation of the [ListLevel](../) object for the specified index of the list item"
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
| index | int | The index of the list item (must be in the range from 1 to 32767). |
| number_style | [NumberStyle](../../../aspose.words/numberstyle/) | The [NumberStyle](../../../aspose.words/numberstyle/) of the [ListLevel](../) object. |
| custom_number_style_format | str | The optional format string used when [NumberStyle.CUSTOM](../../../aspose.words/numberstyle/#CUSTOM) is specified (e.g. "a, ç, ĝ, ..."). In other cases, this parameter must be ``None`` or empty. |

### Returns

The string representation of the [ListLevel](../) object, described by the *numberStyle* parameter and
the*customNumberStyleFormat* parameter, in the list item at the position determined by the*index* parameter.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | *customNumberStyleFormat* is``None`` or empty when the *numberStyle* is custom.-or-*customNumberStyleFormat* is not``None`` or empty when the *numberStyle* is non-custom.-or-*customNumberStyleFormat* is invalid. |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | index is out of range. |

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

