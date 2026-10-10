---
title: "Aspose::Words::Section::get_ProtectedForForms méthode"
linktitle: "get_ProtectedForForms"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Section::get_ProtectedForForms méthode. Vrai si la section est protégée pour les formulaires. Lorsqu'une section est protégée pour les formulaires, les utilisateurs ne peuvent sélectionner et modifier le texte que dans les champs de formulaire dans Microsoft Word en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words/section/get_protectedforforms/
---
## Section::get_ProtectedForForms method


Vrai si la section est protégée pour les formulaires. Lorsqu'une section est protégée pour les formulaires, les utilisateurs ne peuvent sélectionner et modifier le texte que dans les champs de formulaire dans Microsoft Word.

```cpp
bool Aspose::Words::Section::get_ProtectedForForms()
```


## Exemples



Montre comment désactiver la protection d'une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Appliquer la protection en écriture à chaque section du document.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Désactiver la protection en écriture pour la première section.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// Dans ce document de sortie, nous pourrons modifier librement la première section,
// et nous ne pourrons modifier que le contenu du champ de formulaire dans la deuxième section.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## Voir aussi

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
