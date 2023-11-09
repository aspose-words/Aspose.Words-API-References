---
title: Fill.back_tint_and_shade property
linktitle: back_tint_and_shade property
articleTitle: back_tint_and_shade property
second_title: Aspose.Words for Python
description: "Fill.back_tint_and_shade property. Gets or sets a double value that lightens or darkens the background color."
type: docs
weight: 30
url: /python-net/aspose.words.drawing/fill/back_tint_and_shade/
---

## Fill.back_tint_and_shade property

Gets or sets a double value that lightens or darkens the background color.


```python
@property
def back_tint_and_shade(self) -> float:
    ...

@back_tint_and_shade.setter
def back_tint_and_shade(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throw if set this property to a value less than -1 or more than 1. |

### Remarks

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.

Zero (0) is neutral.




### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

