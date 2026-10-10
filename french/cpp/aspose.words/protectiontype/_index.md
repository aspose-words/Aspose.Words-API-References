---
title: "Énumération Aspose::Words::ProtectionType"
linktitle: "ProtectionType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::ProtectionType. Type de protection pour un document en C++."
type: docs
weight: 111000
url: /fr/cpp/aspose.words/protectiontype/
---
## ProtectionType enum


Type de protection pour un document.

```cpp
enum class ProtectionType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| AllowOnlyComments | 1 | L'utilisateur ne peut modifier que les commentaires dans le document. |
| AllowOnlyFormFields | 2 | L'utilisateur ne peut saisir des données que dans les champs de formulaire du document. |
| AllowOnlyRevisions | 0 | L'utilisateur ne peut ajouter que des marques de révision au document. |
| ReadOnly | 3 | Aucun changement n'est autorisé dans le document. Disponible depuis Microsoft Word 2003. |
| NoProtection | -1 | Le document n'est pas protégé. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
