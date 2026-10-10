---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Keywords metodu"
linktitle: "get_Keywords"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Keywords metodu. Belgede anahtar kelimeleri C++'ta alır veya ayarlar."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_keywords/
---
## BuiltInDocumentProperties::get_Keywords method


Belge anahtar kelimelerini alır veya ayarlar.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Keywords()
```


## Örnekler



Yerleşik belge özellikleriyle "Description" kategorisinde nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Aşağıda, belge gövdesinde değerlerini görüntüleyebilen alanlara sahip dört yerleşik belge özelliği bulunmaktadır.
// 1 -  \"Author\" özelliği, AUTHOR alanı kullanarak görüntüleyebiliriz:
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true);

// 2 -  \"Title\" özelliği, TITLE alanı kullanarak görüntüleyebiliriz:
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, true);

// 3 -  \"Subject\" özelliği, SUBJECT alanı kullanarak görüntüleyebiliriz:
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true);

// 4 -  \"Comments\" özelliği, COMMENTS alanı kullanarak görüntüleyebiliriz:
properties->set_Comments(System::String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true);
builder->Write(u"\"");

// \"Category\" yerleşik özelliğinin değerini görüntüleyebilecek bir alanı yoktur.
properties->set_Category(u"My category");

// \"Keywords\" özelliğinin dize değerini noktalı virgüllerle ayırarak bir belge için birden fazla anahtar kelime ayarlayabiliriz.
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// Windows Gezgini'nde bu belgeye sağ tıklayarak bu özellikleri \"Properties\" -> \"Details\" içinde bulabiliriz.
// \"Author\" yerleşik özelliği \"Origin\" grubunda, diğerleri ise \"Description\" grubundadır.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Description.docx");
```

## Ayrıca Bakınız

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
