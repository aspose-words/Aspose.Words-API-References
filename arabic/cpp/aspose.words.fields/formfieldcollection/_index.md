---
title: "Aspose::Words::Fields::FormFieldCollection class"
linktitle: "FormFieldCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FormFieldCollection class. مجموعة من كائنات FormField التي تمثل جميع حقول النموذج في نطاق. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 113000
url: /ar/cpp/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class


مجموعة من كائنات [FormField](../formfield/) التي تمثل جميع حقول النموذج في نطاق. لمعرفة المزيد، زر مقالة الوثائق [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormFieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::FormField>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clear](./clear/)() | يزيل جميع حقول النموذج من هذه المجموعة ومن المستند. |
| [get_Count](./get_count/)() | يرجع عدد حقول النموذج في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يرجع حقل نموذج في الفهرس المحدد. |
| [idx_get](./idx_get/)(const System::String\&) | يرجع حقل نموذج حسب اسم العلامة المرجعية. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | يزيل حقل نموذج بالاسم المحدد. |
| [RemoveAt](./removeat/)(int32_t) | يزيل حقل نموذج في الفهرس المحدد. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
