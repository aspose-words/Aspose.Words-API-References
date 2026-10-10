---
title: "طريقة Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture"
linktitle: "GetCulture"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture. تُرجع كائن CultureInfo لاستخدامه أثناء تحديث الحقل في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider::GetCulture method


تُرجع كائن **CultureInfo** لاستخدامه أثناء تحديث الحقل.

```cpp
virtual System::SharedPtr<System::Globalization::CultureInfo> Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture(System::String culture, System::SharedPtr<Aspose::Words::Fields::Field> field)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| الثقافة | System::String | اسم الثقافة المطلوبة للحقول التي يتم تحديثها. |
| حقل | System::SharedPtr\<Aspose::Words::Fields::Field\> | الحقل الذي يتم تحديثه. |

### ReturnValue

كائن الثقافة الذي يجب استخدامه لتحديث الحقل.

## انظر أيضًا

* Class [Field](../../field/)
* Interface [IFieldUpdateCultureProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
