---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Comments metod"
linktitle: "get_Comments"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Comments metod. Hämtar eller anger dokumentkommentarerna i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.properties/builtindocumentproperties/get_comments/
---
## BuiltInDocumentProperties::get_Comments method


Hämtar eller anger dokumentkommentarerna.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Comments()
```


## Exempel



Visar hur man arbetar med inbyggda dokumentegenskaper i kategorin "Description".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Nedan följer fyra inbyggda dokumentegenskaper som har fält som kan visa sina värden i dokumentets brödtext.
// 1 -  "Author"-egenskapen, som vi kan visa med ett AUTHOR-fält:
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true);

// 2 -  "Title"-egenskapen, som vi kan visa med ett TITLE-fält:
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, true);

// 3 -  "Subject"-egenskapen, som vi kan visa med ett SUBJECT-fält:
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true);

// 4 -  "Comments"-egenskapen, som vi kan visa med ett COMMENTS-fält:
properties->set_Comments(System::String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true);
builder->Write(u"\"");

// Den inbyggda egenskapen "Category" har inget fält som kan visa dess värde.
properties->set_Category(u"My category");

// Vi kan ange flera nyckelord för ett dokument genom att separera strängvärdet för egenskapen "Keywords" med semikolon.
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// Vi kan högerklicka på detta dokument i Windows Explorer och hitta dessa egenskaper i "Properties" -> "Details".
// Den inbyggda egenskapen "Author" finns i gruppen "Origin", och de andra finns i gruppen "Description".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Description.docx");
```

## Se även

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
