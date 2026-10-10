---
title: "Aspose::Words::Fields::FormFieldCollection sınıfı"
linktitle: "FormFieldCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FormFieldCollection sınıfı. Bir aralıktaki tüm form alanlarını temsil eden FormField nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için C++ belgeleri makalesini ziyaret edin."
type: docs
weight: 113000
url: /tr/cpp/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class


Bir aralıktaki tüm form alanlarını temsil eden [FormField](../formfield/) nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/) belgeleri makalesini ziyaret edin.

```cpp
class FormFieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::FormField>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clear](./clear/)() | Bu koleksiyondan ve belgelerden tüm form alanlarını kaldırır. |
| [get_Count](./get_count/)() | Koleksiyondaki form alanı sayısını döndürür. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki bir form alanını döndürür. |
| [idx_get](./idx_get/)(const System::String\&) | Yer imi adıyla bir form alanını döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Belirtilen adla bir form alanını kaldırır. |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen dizindeki bir form alanını kaldırır. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
