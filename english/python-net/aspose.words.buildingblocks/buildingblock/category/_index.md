﻿---
title: BuildingBlock.category property
linktitle: category property
articleTitle: category property
second_title: Aspose.Words for Python
description: "BuildingBlock.category property. Specifies the second-level categorization for the building block."
type: docs
weight: 30
url: /python-net/aspose.words.buildingblocks/buildingblock/category/
---

## BuildingBlock.category property

Specifies the second-level categorization for the building block.


```python
@property
def category(self) -> str:
    ...

@category.setter
def category(self, value: str):
    ...

```

### Remarks

Building blocks in Microsoft Word user interface are arranged 
into Galleries. Each [BuildingBlock.gallery](../gallery/) can have multiple Categories. Each block within
a [BuildingBlock.category](./) has a [BuildingBlock.name](../name/).

Cannot be ``None`` and cannot be an empty string.

Corresponds to the **docPartPr.category.name** element in OOXML.




### See Also

* module [aspose.words.buildingblocks](../../)
* class [BuildingBlock](../)
* property [BuildingBlock.gallery](../gallery/)
* property [BuildingBlock.name](../name/)

