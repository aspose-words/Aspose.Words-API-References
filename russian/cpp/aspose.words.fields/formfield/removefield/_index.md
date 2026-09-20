---
title: "Метод Aspose::Words::Fields::FormField::RemoveField"
linktitle: "RemoveField"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FormField::RemoveField. Удаляет полностью поле формы, а не только специальный символ поля формы в C++."
type: docs
weight: 27000
url: /ru/cpp/aspose.words.fields/formfield/removefield/
---
## FormField::RemoveField method


Удаляет полностью поле формы, а не только специальный символ поля формы.

```cpp
void Aspose::Words::Fields::FormField::RemoveField()
```


## Примеры



Показывает, как удалить поле формы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(3);
formField->RemoveField();
```

## См. также

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
