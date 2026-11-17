---
title: Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider method
linktitle: get_FieldUpdateCultureProvider
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider method. Gets or sets a provider that returns a culture object specific for each particular field in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.fields/fieldoptions/get_fieldupdatecultureprovider/
---
## FieldOptions::get_FieldUpdateCultureProvider method


Gets or sets a provider that returns a culture object specific for each particular field.

```cpp
const System::SharedPtr<Aspose::Words::Fields::IFieldUpdateCultureProvider> & Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider() const
```

## Remarks


The provider is requested when the value of [FieldUpdateCultureSource](../get_fieldupdateculturesource/) is [FieldCode](../../fieldupdateculturesource/).

If the provider is present, then the culture object it returns is used for the field update. Otherwise, a system culture is used. 
## See Also

* Interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
