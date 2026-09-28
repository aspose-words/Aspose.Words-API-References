---
title: "Метод get_FieldData класса Aspose::Words::Fields::FieldStart"
linktitle: "get_FieldData"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод get_FieldData класса Aspose::Words::Fields::FieldStart. Получает пользовательские данные поля, связанные с полем, в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fields/fieldstart/get_fielddata/
---
## FieldStart::get_FieldData method


Получает пользовательские данные поля, связанные с полем.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::Fields::FieldStart::get_FieldData() const
```


## Примеры



Показывает, как получить данные, связанные с полем.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - Field with data.docx");

System::SharedPtr<Aspose::Words::Fields::Field> field = doc->get_Range()->get_Fields()->idx_get(2);
std::cout << System::Text::Encoding::get_Default()->GetString(field->get_Start()->get_FieldData()) << std::endl;
```

## См. также

* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
