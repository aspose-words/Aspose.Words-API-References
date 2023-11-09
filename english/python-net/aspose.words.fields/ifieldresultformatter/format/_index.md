---
title: IFieldResultFormatter.format method
linktitle: format method
articleTitle: format method
second_title: Aspose.Words for Python
description: "aspose.words.fields.IFieldResultFormatter.format method"
type: docs
weight: 10
url: /python-net/aspose.words.fields/ifieldresultformatter/format/
---

## format(value, format) {#str_generalformat}

Called when Aspose.Words applies a capitalization format switch, i.e. \\\* Upper.


```python
def format(self, value: str, format: aspose.words.fields.GeneralFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | str |  |
| format | [GeneralFormat](../../generalformat/) |  |

### Remarks

The implementation should return ``None`` to indicate that the default formatting should be applied.



## format(value, format) {#float_generalformat}

Called when Aspose.Words applies a number format switch, i.e. \\\* Ordinal.


```python
def format(self, value: float, format: aspose.words.fields.GeneralFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | float |  |
| format | [GeneralFormat](../../generalformat/) |  |

### Remarks

The implementation should return ``None`` to indicate that the default formatting should be applied.



## See Also

* module [aspose.words.fields](../../)
* class [IFieldResultFormatter](../)

