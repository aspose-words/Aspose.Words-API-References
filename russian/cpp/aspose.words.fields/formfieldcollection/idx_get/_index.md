---
title: "Aspose::Words::Fields::FormFieldCollection::idx_get метод"
linktitle: "idx_get"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FormFieldCollection::idx_get метод. Возвращает поле формы по имени закладки в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.fields/formfieldcollection/idx_get/
---
## FormFieldCollection::idx_get(const System::String\&) method


Возвращает поле формы по имени закладки.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::Fields::FormFieldCollection::idx_get(const System::String &bookmarkName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | const System::String\& | Имя закладки без учёта регистра. |

## См. также

* Class [FormField](../../formfield/)
* Class [FormFieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## FormFieldCollection::idx_get(int32_t) method


Возвращает поле формы по указанному индексу.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::Fields::FormFieldCollection::idx_get(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Индекс в коллекции. |
## Примечания


Индекс начинается с нуля.

Отрицательные индексы допускаются и указывают доступ с конца коллекции. Например, -1 означает последний элемент, -2 — предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается нулевая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается нулевая ссылка.

## См. также

* Class [FormField](../../formfield/)
* Class [FormFieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
