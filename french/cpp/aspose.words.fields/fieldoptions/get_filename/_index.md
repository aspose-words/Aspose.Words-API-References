---
title: "Aspose::Words::Fields::FieldOptions::get_FileName méthode"
linktitle: "get_FileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldOptions::get_FileName. Obtient ou définit le nom de fichier du document en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.fields/fieldoptions/get_filename/
---
## FieldOptions::get_FileName method


Obtient ou définit le nom de fichier du document.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_FileName() const
```

## Remarques


Cette propriété est utilisée par le champ [FieldFileName](../../fieldfilename/) avec une priorité supérieure à celle de la propriété [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

## Exemples



Montre comment utiliser [FieldOptions](../) pour remplacer la valeur par défaut du champ FILENAME.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// Ce champ FILENAME affichera le nom de fichier du système local du document que nous avons chargé.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// Par défaut, le champ FILENAME montre le nom du fichier, mais pas son chemin complet sur le système de fichiers local.
// Nous pouvons définir un indicateur pour qu'il affiche le chemin complet du fichier.
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->set_IncludeFullPath(true);
field->Update();

ASSERT_EQ(get_MyDir() + u"Document.docx", field->get_Result());

// Nous pouvons également définir une valeur pour cette propriété à
// remplacer la valeur affichée par le champ FILENAME.
doc->get_FieldOptions()->set_FileName(u"FieldOptions.FILENAME.docx");
field->Update();

ASSERT_EQ(u" FILENAME  \\p", field->GetFieldCode());
ASSERT_EQ(u"FieldOptions.FILENAME.docx", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + doc->get_FieldOptions()->get_FileName());
```

## Voir aussi

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
