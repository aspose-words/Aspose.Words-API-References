---
title: "Aspose::Words::Settings::WriteProtection::SetPassword méthode"
linktitle: "SetPassword"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::WriteProtection::SetPassword méthode. Définit le mot de passe de protection en écriture du document en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection::SetPassword method


Définit le mot de passe de protection en écriture du document.

```cpp
void Aspose::Words::Settings::WriteProtection::SetPassword(const System::String &password)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| password | const System::String\& | Le mot de passe à définir. Ne peut pas être **null**, mais peut être une chaîne vide. |
## Remarques


Si un mot de passe est défini, Microsoft Word demandera à l'utilisateur de le saisir ou ouvrira le document en lecture seule.

## Exemples



Montre comment protéger un document avec un mot de passe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// Saisissez un mot de passe d'une longueur maximale de 15 caractères, puis vérifiez l'état de protection du document.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// La protection n'empêche pas le document d'être modifié par programme, ni ne chiffre le contenu.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## Voir aussi

* Class [WriteProtection](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
