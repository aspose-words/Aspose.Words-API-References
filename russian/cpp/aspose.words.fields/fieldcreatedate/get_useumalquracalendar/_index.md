---
title: "Метод Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar. Получает или задает, использовать ли календарь Ум-аль-Кура в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fields/fieldcreatedate/get_useumalquracalendar/
---
## FieldCreateDate::get_UseUmAlQuraCalendar method


Получает или задает, использовать ли календарь Um-al-Qura.

```cpp
bool Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar() override
```


## Примеры



Показывает, как использовать поле CREATEDATE для отображения даты/времени создания документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// Мы можем использовать поле CREATEDATE для отображения даты и времени создания документа.
// Ниже представлены три различных типа календарей, в соответствии с которыми поле CREATEDATE может отображать дату/время.
// 1 -  Исламский лунный календарь:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  Календарь Umm al-Qura:
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  Индийский национальный календарь:
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CREATEDATE.docx");
```

## См. также

* Class [FieldCreateDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
