---
title: Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture method
linktitle: GetCulture
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture method. Returns a CultureInfo object to be used during the field''s update in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider::GetCulture method


Returns a **CultureInfo** object to be used during the field's update.

```cpp
virtual System::SharedPtr<System::Globalization::CultureInfo> Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture(System::String culture, System::SharedPtr<Aspose::Words::Fields::Field> field)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| culture | System::String | The name of the culture requested for the field being updated. |
| field | System::SharedPtr\<Aspose::Words::Fields::Field\> | The field being updated. |

### ReturnValue

The culture object that should be used for the field's update.

## See Also

* Class [Field](../../field/)
* Interface [IFieldUpdateCultureProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
