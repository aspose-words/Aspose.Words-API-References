---
title: "Méthode Aspose::Words::Saving::TxtListIndentation::get_Count"
linktitle: "get_Count"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::TxtListIndentation::get_Count. Obtient ou définit le nombre de caractères à utiliser comme indentation par niveau de liste. La valeur par défaut est 0, ce qui signifie aucune indentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/txtlistindentation/get_count/
---
## TxtListIndentation::get_Count method


Obtient ou définit le nombre de [Character](../get_character/) à utiliser comme indentation par niveau de liste. La valeur par défaut est 0, ce qui signifie aucune indentation.

```cpp
int32_t Aspose::Words::Saving::TxtListIndentation::get_Count() const
```


## Exemples



Montre comment configurer l'indentation des listes lors de l'enregistrement d'un document en texte brut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez une liste avec trois niveaux d'indentation.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// Créez un objet "TxtSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Définissez la propriété "Character" pour assigner un caractère à utiliser
// pour le remplissage qui simule l'indentation des listes en texte brut.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// Définissez la propriété "Count" pour spécifier le nombre de fois
// de placer le caractère de remplissage pour chaque niveau d'indentation de liste.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## Voir aussi

* Class [TxtListIndentation](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
