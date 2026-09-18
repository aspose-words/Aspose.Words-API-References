---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Title Methode"
linktitle: "get_Title"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Title Methode. Gibt den Titel des Dokuments zurück oder setzt ihn in C++."
type: docs
weight: 29000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_title/
---
## BuiltInDocumentProperties::get_Title method


Liest oder setzt den Titel des Dokuments.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Title()
```


## Beispiele



Zeigt, wie man mit integrierten Dokumenteigenschaften in der Kategorie "Description" arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Unten sind vier integrierte Dokumenteigenschaften aufgeführt, die Felder besitzen, die ihre Werte im Dokumentkörper anzeigen können.
// 1 -  "Author"-Eigenschaft, die wir mit einem AUTHOR-Feld anzeigen können:
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true);

// 2 -  "Title"-Eigenschaft, die wir mit einem TITLE-Feld anzeigen können:
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, true);

// 3 -  "Subject"-Eigenschaft, die wir mit einem SUBJECT-Feld anzeigen können:
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true);

// 4 -  "Comments"-Eigenschaft, die wir mit einem COMMENTS-Feld anzeigen können:
properties->set_Comments(System::String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true);
builder->Write(u"\"");

// Die integrierte Eigenschaft "Category" hat kein Feld, das ihren Wert anzeigen kann.
properties->set_Category(u"My category");

// Wir können mehrere Schlüsselwörter für ein Dokument festlegen, indem wir den Zeichenfolgenwert der "Keywords"-Eigenschaft durch Semikolons trennen.
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// Wir können dieses Dokument im Windows Explorer mit der rechten Maustaste anklicken und diese Eigenschaften unter "Properties" -> "Details" finden.
// Die "Author" eingebaute Eigenschaft befindet sich in der "Origin" Gruppe, und die anderen befinden sich in der "Description" Gruppe.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Description.docx");
```

## Siehe auch

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
