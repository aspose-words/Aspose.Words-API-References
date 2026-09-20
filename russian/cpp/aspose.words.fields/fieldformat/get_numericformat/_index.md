---
title: "Aspose::Words::Fields::FieldFormat::get_NumericFormat метод"
linktitle: "get_NumericFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldFormat::get_NumericFormat метод. Получает или задает форматирование, применяемое к результату числового поля. Соответствует переключателю \\# в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fields/fieldformat/get_numericformat/
---
## FieldFormat::get_NumericFormat method


Получает или задаёт форматирование, применяемое к результату числового поля. Соответствует переключателю \\#.

```cpp
System::String Aspose::Words::Fields::FieldFormat::get_NumericFormat()
```


## Примеры



Показывает, как форматировать результаты полей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Используйте DocumentBuilder, чтобы вставить поле, отображающее результат без применённого формата.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// Мы можем применить формат к результату поля, используя свойства поля.
// Ниже представлены три типа форматов, которые мы можем применить к результату поля.
// 1 -  Числовой формат:
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 -  Формат даты/времени:
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 -  Общий формат:
field = builder->InsertField(u"= 25 + 33");
format = field->get_Format();
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::Upper);
field->Update();

int32_t index = 0;
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<Aspose::Words::Fields::GeneralFormat>> generalFormatEnumerator = format->get_GeneralFormats()->GetEnumerator();
    while (generalFormatEnumerator->MoveNext())
    {
        std::cout << System::String::Format(u"General format index {0}: {1}", index++, generalFormatEnumerator->get_Current()) << std::endl;
    }
}

ASSERT_EQ(u"= 25 + 33 \\* roman \\* Upper", field->GetFieldCode());
ASSERT_EQ(u"LVIII", field->get_Result());
ASSERT_EQ(2, format->get_GeneralFormats()->get_Count());
ASSERT_EQ(Aspose::Words::Fields::GeneralFormat::LowercaseRoman, format->get_GeneralFormats()->idx_get(0));

// Мы можем удалить наши форматы, чтобы вернуть результат поля к исходному виду.
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## См. также

* Class [FieldFormat](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
