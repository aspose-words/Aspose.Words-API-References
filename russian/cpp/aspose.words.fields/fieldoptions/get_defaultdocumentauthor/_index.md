---
title: "Метод Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor"
linktitle: "get_DefaultDocumentAuthor"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor. Получает или задает имя автора документа по умолчанию. Если имя автора уже указано во встроенных свойствах документа, эта опция не учитывается в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.fields/fieldoptions/get_defaultdocumentauthor/
---
## FieldOptions::get_DefaultDocumentAuthor method


Получает или задает имя автора документа по умолчанию. Если имя автора уже указано во встроенных свойствах документа, эта опция не учитывается.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor() const
```


## Примеры



Показывает, как использовать поле AUTHOR для отображения имени создателя документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поля AUTHOR получают свои результаты из встроенного свойства документа под названием "Author".
// Если мы создаём и сохраняем документ в Microsoft Word,
// в этом свойстве будет указано наше имя пользователя.
// Однако, если мы создаём документ программно с помощью Aspose.Words,
// свойство "Author" по умолчанию будет пустой строкой.
ASSERT_EQ(System::String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// Установите резервное имя автора для использования полями AUTHOR
// если свойство "Author" содержит пустую строку.
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// Обновление поля AUTHOR, содержащего значение
// применит это значение к встроенному свойству "Author".
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// Изменив это свойство, а затем обновив поле AUTHOR, вы примените это значение к полю.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// Если мы обновим поле AUTHOR после изменения его свойства "Name",
// тогда поле отобразит новое имя и применит новое имя к встроенному свойству.
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// Поля AUTHOR не влияют на свойство DefaultDocumentAuthor.
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(get_ArtifactsDir() + u"Field.AUTHOR.docx");
```

## См. также

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
