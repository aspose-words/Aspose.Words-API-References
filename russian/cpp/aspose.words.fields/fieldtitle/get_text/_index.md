---
title: "Метод Aspose::Words::Fields::FieldTitle::get_Text"
linktitle: "get_Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldTitle::get_Text. Получает или задает текст заголовка в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldtitle/get_text/
---
## FieldTitle::get_Text method


Получает или задает текст заголовка.

```cpp
System::String Aspose::Words::Fields::FieldTitle::get_Text()
```


## Примеры



Показывает, как использовать поле TITLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Установите значение для встроенного свойства документа \"Title\".
doc->get_BuiltInDocumentProperties()->set_Title(u"My Title");

// Мы можем использовать поле TITLE, чтобы отобразить значение этого свойства в документе.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->Update();

ASSERT_EQ(u" TITLE ", field->GetFieldCode());
ASSERT_EQ(u"My Title", field->get_Result());

// Установка значения свойства Text поля,
// а затем обновление поля также перезапишет соответствующее встроенное свойство новым значением.
builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->set_Text(u"My New Title");
field->Update();

ASSERT_EQ(u" TITLE  \"My New Title\"", field->GetFieldCode());
ASSERT_EQ(u"My New Title", field->get_Result());
ASSERT_EQ(u"My New Title", doc->get_BuiltInDocumentProperties()->get_Title());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TITLE.docx");
```

## См. также

* Class [FieldTitle](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
