---
title: "Метод Aspose::Words::Document::get_RemovePersonalInformation"
linktitle: "get_RemovePersonalInformation"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_RemovePersonalInformation. Получает или задает флаг, указывающий, что Microsoft Word будет удалять всю пользовательскую информацию из комментариев, исправлений и свойств документа при сохранении документа в C++."
type: docs
weight: 45000
url: /ru/cpp/aspose.words/document/get_removepersonalinformation/
---
## Document::get_RemovePersonalInformation method


Получает или задает флаг, указывающий, что Microsoft Word будет удалять всю пользовательскую информацию из комментариев, правок и свойств документа при сохранении.

```cpp
bool Aspose::Words::Document::get_RemovePersonalInformation()
```


## Примеры



Показывает, как включить удаление персональной информации при ручном сохранении.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте некоторый контент с персональной информацией.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
doc->get_BuiltInDocumentProperties()->set_Company(u"Placeholder Inc.");

doc->StartTrackRevisions(doc->get_BuiltInDocumentProperties()->get_Author(), System::DateTime::get_Now());
builder->Write(u"Hello world!");
doc->StopTrackRevisions();

// Этот флаг эквивалентен File -> Options -> Trust Center -> Trust Center Settings... ->
// Privacy Options -> "Remove personal information from file properties on save" в Microsoft Word.
doc->set_RemovePersonalInformation(saveWithoutPersonalInfo);

// Эта опция не будет применяться во время операции сохранения, выполненной с помощью Aspose.Words.
// Персональные данные будут удалены из нашего документа при установленном флаге, когда мы сохраняем его вручную с помощью Microsoft Word.
doc->Save(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");

ASPOSE_ASSERT_EQ(saveWithoutPersonalInfo, doc->get_RemovePersonalInformation());
ASSERT_EQ(u"John Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Placeholder Inc.", doc->get_BuiltInDocumentProperties()->get_Company());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
