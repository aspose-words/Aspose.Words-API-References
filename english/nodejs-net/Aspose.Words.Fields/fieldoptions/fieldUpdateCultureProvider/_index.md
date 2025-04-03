---
title: FieldOptions.fieldUpdateCultureProvider property
linktitle: fieldUpdateCultureProvider property
articleTitle: fieldUpdateCultureProvider property
second_title: Aspose.Words for NodeJs
description: "FieldOptions.fieldUpdateCultureProvider property. Gets or sets a provider that returns a culture object specific for each particular field."
type: docs
weight: 90
url: /nodejs-net/aspose.words.fields/fieldoptions/fieldUpdateCultureProvider/
---

## FieldOptions.fieldUpdateCultureProvider property

Gets or sets a provider that returns a culture object specific for each particular field.


```js
get fieldUpdateCultureProvider(): Aspose.Words.Fields.IFieldUpdateCultureProvider
```

### Remarks

The provider is requested when the value of [FieldOptions.fieldUpdateCultureSource](../fieldUpdateCultureSource/) is [FieldUpdateCultureSource.FieldCode](../../fieldupdateculturesource/#FieldCode).

If the provider is present, then the culture object it returns is used for the field update. Otherwise, a system culture is used.




### See Also

* module [Aspose.Words.Fields](../../)
* class [FieldOptions](../)

