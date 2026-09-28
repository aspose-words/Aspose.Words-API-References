---
title: "Aspose::Words::Fields::FieldSaveDate::get_UseUmAlQuraCalendar метод"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldSaveDate::get_UseUmAlQuraCalendar метод. Получает или задает, использовать ли календарь Um-al-Qura в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fields/fieldsavedate/get_useumalquracalendar/
---
## FieldSaveDate::get_UseUmAlQuraCalendar method


Получает или задает, использовать ли календарь Um-al-Qura.

```cpp
bool Aspose::Words::Fields::FieldSaveDate::get_UseUmAlQuraCalendar() override
```


## Примеры



Показывает, как использовать поле SAVEDATE для отображения даты/времени последней операции сохранения документа, выполненной в Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Мы можем использовать поле SAVEDATE для отображения даты и времени последней операции сохранения в документе.
// Операция сохранения, к которой относятся эти поля, — это ручное сохранение в приложении, таком как Microsoft Word,
// а не метод Save документа.
// Ниже представлены три разных типа календарей, в соответствии с которыми поле SAVEDATE может отображать дату/время.
// 1 -  Исламский лунный календарь:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Календарь Umm al-Qura:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 -  Индийский национальный календарь:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// Поля SAVEDATE берут свои значения даты/времени из встроенного свойства LastSavedTime.
// Метод Save документа не будет обновлять это значение, но мы всё равно можем обновить его вручную.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## См. также

* Class [FieldSaveDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
