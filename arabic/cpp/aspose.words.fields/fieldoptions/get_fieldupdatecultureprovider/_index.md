---
title: "طريقة Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider"
linktitle: "get_FieldUpdateCultureProvider"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider. يحصل على أو يعيّن موفرًا يُعيد كائن ثقافة مخصص لكل حقل معين في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.fields/fieldoptions/get_fieldupdatecultureprovider/
---
## FieldOptions::get_FieldUpdateCultureProvider method


الحصول على أو تعيين موفر يُعيد كائن ثقافة مخصص لكل حقل على حدة.

```cpp
const System::SharedPtr<Aspose::Words::Fields::IFieldUpdateCultureProvider> & Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider() const
```

## ملاحظات


يُطلب الموفر عندما تكون قيمة [FieldUpdateCultureSource](../get_fieldupdateculturesource/) هي [FieldCode](../../fieldupdateculturesource/).

إذا كان الموفر موجودًا، فسيُستخدم كائن الثقافة الذي يُعيده لتحديث الحقل. وإلا، سيتم استخدام ثقافة النظام.
## انظر أيضًا

* Interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
