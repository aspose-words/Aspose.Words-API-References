---
title: "Méthode Aspose::Words::Document::get_ProtectionType"
linktitle: "get_ProtectionType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::get_ProtectionType. Obtient le type de protection du document actuellement actif en C++."
type: docs
weight: 44000
url: /fr/cpp/aspose.words/document/get_protectiontype/
---
## Document::get_ProtectionType method


Obtient le type de protection du document actuellement actif.

```cpp
Aspose::Words::ProtectionType Aspose::Words::Document::get_ProtectionType()
```

## Remarques


Cette propriété permet de récupérer le type de protection du document actuellement défini. Pour modifier le type de protection du document, utilisez les méthodes [Protect()](../) et [Unprotect](../unprotect/).

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
