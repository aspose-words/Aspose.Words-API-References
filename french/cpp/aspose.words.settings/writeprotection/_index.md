---
title: "Classe Aspose::Words::Settings::WriteProtection"
linktitle: "WriteProtection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Settings::WriteProtection. Spécifie les paramètres de protection en écriture d'un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.settings/writeprotection/
---
## WriteProtection class


Spécifie les paramètres de protection en écriture d'un document. Pour en savoir plus, consultez l'article de documentation [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class WriteProtection : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_IsWriteProtected](./get_iswriteprotected/)() | Renvoie **true** lorsqu'un mot de passe de protection en écriture est défini. |
| [get_ReadOnlyRecommended](./get_readonlyrecommended/)() const | Spécifie si l'auteur du document a recommandé que le document soit ouvert en lecture seule. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ReadOnlyRecommended](./set_readonlyrecommended/)(bool) | Définisseur pour [Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended](./get_readonlyrecommended/). |
| [SetPassword](./setpassword/)(const System::String\&) | Définit le mot de passe de protection en écriture du document. |
| static [Type](./type/)() |  |
| [ValidatePassword](./validatepassword/)(const System::String\&) | Renvoie **true** si le mot de passe spécifié est identique au mot de passe de protection en écriture avec lequel le document a été protégé. Si le document n'est pas protégé en écriture par un mot de passe, il renvoie **false**. |
## Remarques


La protection en écriture spécifie si l'auteur a recommandé que le document soit ouvert en lecture seule et/ou nécessite un mot de passe pour modifier le document.

La protection en écriture est différente de la protection du document. La protection en écriture est spécifiée dans Microsoft Word dans les options de la boîte de dialogue Enregistrer sous.

Vous ne créez pas d'instances de cette classe directement. Vous accédez aux paramètres de protection du document via la propriété [WriteProtection](../../aspose.words/document/get_writeprotection/).

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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
