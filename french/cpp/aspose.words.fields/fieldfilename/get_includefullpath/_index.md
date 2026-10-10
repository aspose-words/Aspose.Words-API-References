---
title: "Méthode Aspose::Words::Fields::FieldFileName::get_IncludeFullPath"
linktitle: "get_IncludeFullPath"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldFileName::get_IncludeFullPath. Obtient ou définit si le chemin complet du fichier doit être inclus en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldfilename/get_includefullpath/
---
## FieldFileName::get_IncludeFullPath method


Obtient ou définit si le nom complet du chemin du fichier doit être inclus.

```cpp
bool Aspose::Words::Fields::FieldFileName::get_IncludeFullPath()
```


## Exemples



Montre comment utiliser [FieldOptions](../../fieldoptions/) pour remplacer la valeur par défaut du champ FILENAME.
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

* Class [FieldFileName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
