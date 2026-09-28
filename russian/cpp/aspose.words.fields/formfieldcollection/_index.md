---
title: "Aspose::Words::Fields::FormFieldCollection класс"
linktitle: "FormFieldCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FormFieldCollection класс. Коллекция объектов FormField, представляющих все поля формы в диапазоне. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 113000
url: /ru/cpp/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class


Коллекция объектов [FormField](../formfield/), представляющих все поля формы в диапазоне. Чтобы узнать больше, посетите статью документации [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormFieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::FormField>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clear](./clear/)() | Удаляет все поля формы из этой коллекции и из документа. |
| [get_Count](./get_count/)() | Возвращает количество полей формы в коллекции. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект перечислителя. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Возвращает поле формы по указанному индексу. |
| [idx_get](./idx_get/)(const System::String\&) | Возвращает поле формы по имени закладки. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Удаляет поле формы с указанным именем. |
| [RemoveAt](./removeat/)(int32_t) | Удаляет поле формы по указанному индексу. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
