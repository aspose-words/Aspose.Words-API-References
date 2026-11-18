---
title: Aspose::Words::Fields::FieldOptions::set_FieldUpdateCultureProvider method
linktitle: set_FieldUpdateCultureProvider
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::set_FieldUpdateCultureProvider method. Sets a provider that returns a culture object specific for each particular field in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words.fields/fieldoptions/set_fieldupdatecultureprovider/
---
## FieldOptions::set_FieldUpdateCultureProvider method


Sets a provider that returns a culture object specific for each particular field.

```cpp
void Aspose::Words::Fields::FieldOptions::set_FieldUpdateCultureProvider(const System::SharedPtr<Aspose::Words::Fields::IFieldUpdateCultureProvider> & value)
```

## Remarks


The provider is requested when the value of [FieldUpdateCultureSource](../get_fieldupdateculturesource/) is [FieldCode](../../fieldupdateculturesource/).

If the provider is present, then the culture object it returns is used for the field update. Otherwise, a system culture is used.
## See Also

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
