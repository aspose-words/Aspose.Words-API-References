---
title: "Aspose::Words::Document::get_WriteProtection méthode"
linktitle: "get_WriteProtection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_WriteProtection méthode. Fournit l'accès aux options de protection en écriture du document en C++."
type: docs
weight: 61000
url: /fr/cpp/aspose.words/document/get_writeprotection/
---
## Document::get_WriteProtection method


Fournit l'accès aux options de protection en écriture du document.

```cpp
System::SharedPtr<Aspose::Words::Settings::WriteProtection> Aspose::Words::Document::get_WriteProtection()
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

* Class [WriteProtection](../../../aspose.words.settings/writeprotection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
