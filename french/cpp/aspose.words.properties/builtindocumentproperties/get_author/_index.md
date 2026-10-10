---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Author méthode"
linktitle: "get_Author"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Author méthode. Obtient ou définit le nom de l’auteur du document en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_author/
---
## BuiltInDocumentProperties::get_Author method


Obtient ou définit le nom de l'auteur du document.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Author()
```


## Exemples



Montre comment travailler avec les propriétés de document intégrées dans la catégorie "Description".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Ci-dessous, quatre propriétés de document intégrées possèdent des champs pouvant afficher leurs valeurs dans le corps du document.
// 1 -  \"Author\" propriété, que nous pouvons afficher à l'aide d'un champ AUTHOR:
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true);

// 2 -  \"Title\" propriété, que nous pouvons afficher à l'aide d'un champ TITLE:
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, true);

// 3 -  \"Subject\" propriété, que nous pouvons afficher à l'aide d'un champ SUBJECT:
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true);

// 4 -  \"Comments\" propriété, que nous pouvons afficher à l'aide d'un champ COMMENTS:
properties->set_Comments(System::String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true);
builder->Write(u"\"");

// La propriété intégrée \"Category\" n'a pas de champ pouvant afficher sa valeur.
properties->set_Category(u"My category");

// Nous pouvons définir plusieurs mots‑clés pour un document en séparant la valeur chaîne de la propriété \"Keywords\" par des points‑virgules.
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// Nous pouvons faire un clic droit sur ce document dans l'Explorateur Windows et trouver ces propriétés dans \"Properties\" -> \"Details\".
// La propriété intégrée \"Author\" se trouve dans le groupe \"Origin\", et les autres sont dans le groupe \"Description\".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Description.docx");
```

## Voir aussi

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
