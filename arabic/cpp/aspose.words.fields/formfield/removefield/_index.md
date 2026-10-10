---
title: "Aspose::Words::Fields::FormField::RemoveField طريقة"
linktitle: "RemoveField"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FormField::RemoveField طريقة. يزيل حقل النموذج بالكامل، وليس مجرد الحرف الخاص بحقل النموذج في C++."
type: docs
weight: 27000
url: /ar/cpp/aspose.words.fields/formfield/removefield/
---
## FormField::RemoveField method


يزيل حقل النموذج بالكامل، وليس مجرد الحرف الخاص بحقل النموذج.

```cpp
void Aspose::Words::Fields::FormField::RemoveField()
```


## أمثلة



يعرض كيفية حذف حقل نموذج.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(3);
formField->RemoveField();
```

## انظر أيضًا

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
