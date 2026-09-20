---
title: "Aspose::Words::Fields::FieldDate::get_UseLastFormat метод"
linktitle: "get_UseLastFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldDate::get_UseLastFormat метод. Получает или задает, использовать ли формат, последний использованный хост‑приложением при вставке нового поля DATE в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fielddate/get_uselastformat/
---
## FieldDate::get_UseLastFormat method


Получает или задает, использовать ли формат, последний использованный хост-приложением при вставке нового поля DATE.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseLastFormat()
```


## Примеры



Показывает, как использовать поля DATE для отображения дат в соответствии с различными типами календарей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Если мы хотим, чтобы текст в документе всегда отображал правильную дату, мы можем использовать поле DATE.
// Ниже представлены три типа культурных календарей, которые поле DATE может использовать для отображения даты.
// 1 -  Исламский лунный календарь:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Календарь Umm al-Qura:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Индийский национальный календарь:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Вставьте поле DATE и задайте его тип календаря, последний использованный хост-приложением.
// В Microsoft Word тип будет тем, который был использован последним в диалоговом окне Вставка -> Текст -> Дата и время.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## См. также

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
