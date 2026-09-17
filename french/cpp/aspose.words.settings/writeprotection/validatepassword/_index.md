---
title: "Aspose::Words::Settings::WriteProtection::ValidatePassword méthode"
linktitle: "ValidatePassword"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::WriteProtection::ValidatePassword méthode. Retourne true si le mot de passe spécifié est identique au mot de passe de protection en écriture avec lequel le document a été protégé. Si le document n'est pas protégé en écriture par un mot de passe, alors retourne false en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection::ValidatePassword method


Renvoie **true** si le mot de passe spécifié est identique au mot de passe de protection en écriture avec lequel le document a été protégé. Si le document n'est pas protégé en écriture par un mot de passe, il renvoie **false**.

```cpp
bool Aspose::Words::Settings::WriteProtection::ValidatePassword(const System::String &password)
```


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
