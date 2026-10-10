---
title: "Méthode Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes"
linktitle: "get_IsInKilobytes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes. Obtient ou définit si la taille du fichier doit être affichée en kilo-octets en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldfilesize/get_isinkilobytes/
---
## FieldFileSize::get_IsInKilobytes method


Obtient ou définit s'il faut afficher la taille du fichier en kilo-octets.

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes()
```


## Exemples



Montre comment afficher la taille du fichier d'un document avec un champ FILESIZE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// Voici trois unités de mesure différentes
// avec lesquelles les champs FILESIZE peuvent afficher la taille du fichier du document.
// 1 -  Octets :
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  Kilo-octets :
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  Mégaoctets :
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// Pour mettre à jour les valeurs de ces champs lors de l'édition dans Microsoft Word,
// nous devons d'abord enregistrer les modifications, puis mettre à jour manuellement ces champs.
doc->Save(get_ArtifactsDir() + u"Field.FILESIZE.docx");
```

## Voir aussi

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
