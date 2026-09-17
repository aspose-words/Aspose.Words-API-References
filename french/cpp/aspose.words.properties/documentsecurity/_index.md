---
title: "Aspose::Words::Properties::DocumentSecurity énumération"
linktitle: "DocumentSecurity"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::DocumentSecurity énum. Utilisé comme valeur pour la propriété Security. Spécifie le niveau de sécurité d'un document sous forme de valeur numérique en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enum


Utilisé comme valeur pour la propriété [Security](../builtindocumentproperties/get_security/). Spécifie le niveau de sécurité d'un document sous forme de valeur numérique.

```cpp
enum class DocumentSecurity
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Il n'y a aucun état de sécurité spécifié par la propriété. |
| PasswordProtected | 1 | Le document est protégé par mot de passe. (Note : cela n'a jamais été observé dans un document jusqu'à présent). |
| ReadOnlyRecommended | 2 | Le document doit être ouvert en lecture seule si possible, mais le paramètre peut être remplacé. |
| ReadOnlyEnforced | 4 | Le document doit toujours être ouvert en lecture seule. |
| ReadOnlyExceptAnnotations | 8 | Le document doit toujours être ouvert en lecture seule, sauf pour les annotations. |


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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
