---
title: "метод Aspose::Words::Properties::BuiltInDocumentProperties::get_Keywords"
linktitle: "get_Keywords"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Properties::BuiltInDocumentProperties::get_Keywords. Получает или задает ключевые слова документа в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/get_keywords/
---
## BuiltInDocumentProperties::get_Keywords method


Получает или задает ключевые слова документа.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Keywords()
```


## Примеры



Показывает, как работать со встроенными свойствами документа в категории \"Description\".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Ниже представлены четыре встроенных свойства документа, которые имеют поля, способные отображать их значения в теле документа.
// 1 -  \"Author\" свойство, которое мы можем отобразить с помощью поля AUTHOR:
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true);

// 2 -  \"Title\" свойство, которое мы можем отобразить с помощью поля TITLE:
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, true);

// 3 -  \"Subject\" свойство, которое мы можем отобразить с помощью поля SUBJECT:
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true);

// 4 -  \"Comments\" свойство, которое мы можем отобразить с помощью поля COMMENTS:
properties->set_Comments(System::String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true);
builder->Write(u"\"");

// У свойства \"Category\" встроенного типа нет поля, которое может отобразить его значение.
properties->set_Category(u"My category");

// Мы можем задать несколько ключевых слов для документа, разделяя строковое значение свойства \"Keywords\" точками с запятой.
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// Мы можем щелкнуть правой кнопкой мыши этот документ в Windows Explorer и найти эти свойства в \"Properties\" -> \"Details\".
// Свойство \"Author\" встроенное находится в группе \"Origin\", а остальные находятся в группе \"Description\".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Description.docx");
```

## См. также

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
