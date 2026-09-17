---
title: "Aspose::Words::Document::Protect méthode"
linktitle: "Protéger"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::Protect méthode. Protège le document contre les modifications sans changer le mot de passe existant ou attribue un mot de passe aléatoire en C++."
type: docs
weight: 67000
url: /fr/cpp/aspose.words/document/protect/
---
## Document::Protect(Aspose::Words::ProtectionType) method


Protège le document contre les modifications sans changer le mot de passe existant ou attribue un mot de passe aléatoire.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| type | Aspose::Words::ProtectionType | Spécifie le type de protection du document. |
## Remarques


Lorsqu'un document est protégé, l'utilisateur ne peut apporter que des modifications limitées, telles que l'ajout d'annotations, la réalisation de révisions ou le remplissage d'un formulaire.

Lorsque vous protégez un document et que le document possède déjà un mot de passe de protection, le mot de passe de protection existant n'est pas modifié.

Lorsque vous protégez un document et que le document ne possède pas de mot de passe de protection, cette méthode attribue un mot de passe aléatoire qui rend impossible la désactivation de la protection du document dans Microsoft Word, mais vous pouvez toujours désactiver la protection du document dans Aspose.Words car aucun mot de passe n'est requis lors de la désactivation.

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

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Protect(Aspose::Words::ProtectionType, const System::String\&) method


Protège le document contre les modifications et définit éventuellement un mot de passe de protection.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type, const System::String &password)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| type | Aspose::Words::ProtectionType | Spécifie le type de protection du document. |
| password | const System::String\& | Le mot de passe avec lequel protéger le document. Spécifiez **null** ou une chaîne vide si vous souhaitez protéger le document sans mot de passe. |
## Remarques


Lorsqu'un document est protégé, l'utilisateur ne peut apporter que des modifications limitées, telles que l'ajout d'annotations, la réalisation de révisions ou le remplissage d'un formulaire.

Notez que la protection du document est différente de la protection en écriture. La protection en écriture est spécifiée à l'aide de [WriteProtection](../get_writeprotection/).

## Exemples



Montre comment protéger et déprotéger un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"password");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// Si nous ouvrons ce document avec Microsoft Word dans le but de le modifier,
// nous devrons saisir le mot de passe pour passer la protection.
doc->Save(get_ArtifactsDir() + u"Document.Protect.docx");

// Notez que la protection ne s'applique qu'aux utilisateurs de Microsoft Word ouvrant notre document.
// Nous n'avons pas chiffré le document de quelque manière que ce soit, et nous n'avons pas besoin du mot de passe pour l'ouvrir et le modifier programmétiquement.
auto protectedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.Protect.docx");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// Il existe deux façons de supprimer la protection d'un document.
// 1 - Sans mot de passe :
doc->Unprotect();

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - Avec le mot de passe correct :
doc->Unprotect(u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());
```

## Voir aussi

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
