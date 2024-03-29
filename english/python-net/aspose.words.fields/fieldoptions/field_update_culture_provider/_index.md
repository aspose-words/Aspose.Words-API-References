﻿---
title: FieldOptions.field_update_culture_provider property
linktitle: field_update_culture_provider property
articleTitle: field_update_culture_provider property
second_title: Aspose.Words for Python
description: "FieldOptions.field_update_culture_provider property. Gets or sets a provider that returns a culture object specific for each particular field."
type: docs
weight: 100
url: /python-net/aspose.words.fields/fieldoptions/field_update_culture_provider/
---

## FieldOptions.field_update_culture_provider property

Gets or sets a provider that returns a culture object specific for each particular field.


```python
@property
def field_update_culture_provider(self) -> aspose.words.fields.IFieldUpdateCultureProvider:
    ...

@field_update_culture_provider.setter
def field_update_culture_provider(self, value: aspose.words.fields.IFieldUpdateCultureProvider):
    ...

```

### Remarks

The provider is requested when the value of [FieldOptions.field_update_culture_source](../field_update_culture_source/) is [FieldUpdateCultureSource.FIELD_CODE](../../fieldupdateculturesource/#FIELD_CODE).

If the provider is present, then the culture object it returns is used for the field update. Otherwise, a system culture is used.




### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

