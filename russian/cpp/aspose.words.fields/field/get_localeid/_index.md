---
title: "Aspose::Words::Fields::Field::get_LocaleId метод"
linktitle: "get_LocaleId"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::Field::get_LocaleId метод. Получает или задает LCID поля в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.fields/field/get_localeid/
---
## Field::get_LocaleId method


Получает или задает LCID поля.

```cpp
int32_t Aspose::Words::Fields::Field::get_LocaleId()
```


## Примеры



Показывает, как вставить поле и работать с его локалью.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте поле DATE, а затем выведите дату, которую оно отобразит.
// Текущая культура вашего потока определяет форматирование даты.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE");
std::cout << System::String::Format(u"Today's date, as displayed in the \"{0}\" culture: {1}", System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName(), field->get_Result()) << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// Изменение культуры нашего потока повлияет на результат поля DATE.
// Другой способ заставить поле DATE отображать дату в другой культуре — использовать его свойство LocaleId.
// Таким способом мы избегаем изменения культуры потока для получения этого эффекта.
doc->get_FieldOptions()->set_FieldUpdateCultureSource(Aspose::Words::Fields::FieldUpdateCultureSource::FieldCode);
auto de = System::MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << System::String::Format(u"Today's date, as displayed according to the \"{0}\" culture: {1}", System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName(), field->get_Result()) << std::endl;
```

## См. также

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
