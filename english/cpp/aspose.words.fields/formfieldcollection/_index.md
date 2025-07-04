---
title: Aspose::Words::Fields::FormFieldCollection class
linktitle: FormFieldCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FormFieldCollection class. A collection of FormField objects that represent all the form fields in a range. To learn more, visit the  documentation article in C++.'
type: docs
weight: 113000
url: /cpp/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class


A collection of [FormField](../formfield/) objects that represent all the form fields in a range. To learn more, visit the [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/) documentation article.

```cpp
class FormFieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::FormField>>
```

## Methods

| Method | Description |
| --- | --- |
| [Clear](./clear/)() | Removes all form fields from this collection and from the document. |
| [get_Count](./get_count/)() | Returns the number of form fields in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returns a form field at the specified index. |
| [idx_get](./idx_get/)(const System::String\&) | Returns a form field by bookmark name. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Removes a form field with the specified name. |
| [RemoveAt](./removeat/)(int32_t) | Removes a form field at the specified index. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
