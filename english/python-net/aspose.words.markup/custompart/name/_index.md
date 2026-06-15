---
title: CustomPart.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "CustomPart.name property. Gets or sets this part's absolute name within the OOXML package or the target URL."
type: docs
weight: 50
url: /python-net/aspose.words.markup/custompart/name/
---

## CustomPart.name property

Gets or sets this part's absolute name within the OOXML package or the target URL.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

### Remarks

If the relationship target is internal, then this property is the absolute part name within the package.
If the relationship target is external, then this property is the target URL.

The default value is an empty string. A valid value must be a non-empty string.




### See Also

* module [aspose.words.markup](../../)
* class [CustomPart](../)
* property [CustomPart.is_external](../is_external/)

