---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security méthode"
linktitle: "get_Security"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security méthode. Spécifie le niveau de sécurité d'un document sous forme de valeur numérique en C++."
type: docs
weight: 25000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_security/
---
## BuiltInDocumentProperties::get_Security method


Spécifie le niveau de sécurité d'un document sous forme de valeur numérique.

```cpp
Aspose::Words::Properties::DocumentSecurity Aspose::Words::Properties::BuiltInDocumentProperties::get_Security()
```

## Remarques


Utilisez cette propriété à des fins d'information uniquement car Microsoft Word ne définit pas toujours cette propriété. Cette propriété n'est disponible que dans les documents DOC et OOXML.

Pour protéger ou déprotéger un document, utilisez les méthodes [Protect()](../) et [Unprotect](../../../aspose.words/document/unprotect/).

Aspose.Words met à jour cette propriété avec une valeur correcte avant d'enregistrer un document.

## Exemples



Montre comment utiliser les propriétés du document pour afficher le niveau de sécurité d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// Si nous configurons un document en lecture seule, il affichera cet état en utilisant la propriété intégrée "Security".
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyRecommended, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// Protégez en écriture un document, puis vérifiez son niveau de sécurité.
doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyEnforced, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// "Security" est une propriété descriptive. Nous pouvons modifier sa valeur manuellement.
doc = System::MakeObject<Aspose::Words::Document>();

doc->Protect(Aspose::Words::ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")->get_BuiltInDocumentProperties()->get_Security());
```

## Voir aussi

* Enum [DocumentSecurity](../../documentsecurity/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
