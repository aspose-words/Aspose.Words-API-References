---
title: "Метод Aspose::Words::Fields::FieldSubject::get_Text"
linktitle: "get_Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldSubject::get_Text. Получает или задает текст субъекта в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldsubject/get_text/
---
## FieldSubject::get_Text method


Получает или задаёт текст темы.

```cpp
System::String Aspose::Words::Fields::FieldSubject::get_Text()
```


## Примеры



Показывает, как использовать поле SUBJECT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Установите значение встроенного свойства документа "Subject".
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// Создайте поле SUBJECT, чтобы отобразить значение этого встроенного свойства.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSubject>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// Если мы зададим значение свойства Text поля SUBJECT и обновим его, поле будет
// перезапишет текущее значение встроенного свойства "Subject" значением его свойства Text,
// а затем отображать новое значение.
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(get_ArtifactsDir() + u"Field.SUBJECT.docx");
```

## См. также

* Class [FieldSubject](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
