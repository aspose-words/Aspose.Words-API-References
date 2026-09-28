---
title: "Метод Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat"
linktitle: "get_LegacyNumberFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat method. Получает или задает значение, указывающее, включён ли устаревший (раньше AW 13.10) формат чисел для полей в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.fields/fieldoptions/get_legacynumberformat/
---
## FieldOptions::get_LegacyNumberFormat method


Получает или задает значение, указывающее, включён ли устаревший (ранний, чем AW 13.10) числовой формат для полей.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat() const
```

## Примечания


Когда это свойство установлено в **true**, шаблонный символ "#" работает как в .net: заменяет знак фунта соответствующей цифрой, если она присутствует; в противном случае в результирующей строке символы не появляются.

Когда это свойство установлено в **false**, шаблонный символ "#" работает как в MS Word: этот элемент формата указывает требуемые числовые позиции для отображения в результате. Если в результате отсутствует цифра в этой позиции, MS Word выводит пробел. Например, { = 9 + 6 \# $### } выводит $ 15.

Значение по умолчанию — **false**.

## Примеры



Показывает, как включить устаревшее форматирование чисел для полей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3 \\# $##");

ASSERT_EQ(u"$ 5", field->get_Result());

doc->get_FieldOptions()->set_LegacyNumberFormat(true);
field->Update();

ASSERT_EQ(u"$5", field->get_Result());
```

## См. также

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
