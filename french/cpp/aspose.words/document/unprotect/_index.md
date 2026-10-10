---
title: "Aspose::Words::Document::Unprotect method"
linktitle: "Déprotéger"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::Unprotect method. Supprime la protection du document quel que soit le mot de passe en C++."
type: docs
weight: 95000
url: /fr/cpp/aspose.words/document/unprotect/
---
## Document::Unprotect() method


Supprime la protection du document quel que soit le mot de passe.

```cpp
void Aspose::Words::Document::Unprotect()
```

## Remarques


Cette méthode déprotège le document même s'il possède un mot de passe de protection.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Unprotect(const System::String\&) method


Supprime la protection du document si un mot de passe correct est spécifié.

```cpp
bool Aspose::Words::Document::Unprotect(const System::String &password)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| password | const System::String\& | Le mot de passe pour déprotéger le document. |

### ReturnValue

**true** if a correct password was specified and the document was unprotected.
## Remarques


Cette méthode déprotège le document uniquement si un mot de passe correct est spécifié.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
