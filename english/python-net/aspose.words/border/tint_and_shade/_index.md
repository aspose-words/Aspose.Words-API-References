---
title: Border.tint_and_shade property
linktitle: tint_and_shade property
articleTitle: tint_and_shade property
second_title: Aspose.Words for Python
description: "Border.tint_and_shade property. Gets or sets a double value that lightens or darkens a color."
type: docs
weight: 80
url: /python-net/aspose.words/border/tint_and_shade/
---

## Border.tint_and_shade property

Gets or sets a double value that lightens or darkens a color.


```python
@property
def tint_and_shade(self) -> float:
    ...

@tint_and_shade.setter
def tint_and_shade(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws if you attempt to set this property to a value less than -1 or more than 1. |
| RuntimeError (Proxy error(InvalidOperationException)) | Throws if setting this property for Border object with non-theme colors. |

### Remarks

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.
Zero (0) is neutral.




### See Also

* module [aspose.words](../../)
* class [Border](../)

