---
title: "Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor méthode"
linktitle: "get_DefaultDocumentAuthor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor méthode. Obtient ou définit le nom de l'auteur du document par défaut. Si le nom de l'auteur est déjà spécifié dans les propriétés intégrées du document, cette option n'est pas prise en compte en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.fields/fieldoptions/get_defaultdocumentauthor/
---
## FieldOptions::get_DefaultDocumentAuthor method


Obtient ou définit le nom d’auteur par défaut du document. Si le nom de l’auteur est déjà spécifié dans les propriétés intégrées du document, cette option n’est pas prise en compte.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor() const
```


## Exemples



Montre comment utiliser un champ AUTHOR pour afficher le nom du créateur du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Les champs AUTHOR tirent leurs résultats de la propriété intégrée du document appelée "Author".
// Si nous créons et enregistrons un document dans Microsoft Word,
// il contiendra notre nom d'utilisateur dans cette propriété.
// Cependant, si nous créons un document de manière programmatique en utilisant Aspose.Words,
// la propriété "Author", par défaut, sera une chaîne vide.
ASSERT_EQ(System::String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// Définissez un nom d'auteur de secours à utiliser par les champs AUTHOR
// si la propriété "Author" contient une chaîne vide.
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// Mise à jour d'un champ AUTHOR contenant une valeur
// appliquera cette valeur à la propriété intégrée "Author".
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// Modifier cette propriété, puis mettre à jour le champ AUTHOR appliquera cette valeur au champ.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// Si nous mettons à jour un champ AUTHOR après avoir modifié sa propriété "Name",
// alors le champ affichera le nouveau nom et appliquera le nouveau nom à la propriété intégrée.
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// Les champs AUTHOR n'affectent pas la propriété DefaultDocumentAuthor.
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(get_ArtifactsDir() + u"Field.AUTHOR.docx");
```

## Voir aussi

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
