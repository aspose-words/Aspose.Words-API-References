---
title: "Aspose::Words::Properties::DocumentPropertyCollection::RemoveAt metodo"
linktitle: "get_Comments"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::DocumentPropertyCollection::RemoveAt metodo. Rimuove una proprietà all'indice specificato in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_comments/
---
## BuiltInDocumentProperties::get_Comments method


Ottiene o imposta i commenti del documento.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Comments()
```


## Esempi



Mostra come lavorare con le proprietà di documento integrate nella categoria "Descrizione".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Di seguito sono elencate quattro proprietà di documento integrate che hanno campi in grado di visualizzare i loro valori nel corpo del documento.
// 1 -  \"Author\" proprietà, che possiamo visualizzare usando un campo AUTHOR:
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true);

// 2 -  \"Title\" proprietà, che possiamo visualizzare usando un campo TITLE:
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, true);

// 3 -  \"Subject\" proprietà, che possiamo visualizzare usando un campo SUBJECT:
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true);

// 4 -  \"Comments\" proprietà, che possiamo visualizzare usando un campo COMMENTS:
properties->set_Comments(System::String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true);
builder->Write(u"\"");

// La proprietà incorporata \"Category\" non ha un campo che possa visualizzare il suo valore.
properties->set_Category(u"My category");

// Possiamo impostare più parole chiave per un documento separando il valore stringa della proprietà \"Keywords\" con punti e virgola.
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// Possiamo fare clic con il tasto destro su questo documento in Windows Explorer e trovare queste proprietà in \"Properties\" -> \"Details\".
// La proprietà incorporata \"Author\" si trova nel gruppo \"Origin\", e le altre si trovano nel gruppo \"Description\".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Description.docx");
```

## Vedi anche

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
