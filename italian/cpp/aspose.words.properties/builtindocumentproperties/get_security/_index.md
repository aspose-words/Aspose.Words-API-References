---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security method"
linktitle: "get_Security"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security method. Specifica il livello di sicurezza di un documento come valore numerico in C++."
type: docs
weight: 25000
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_security/
---
## BuiltInDocumentProperties::get_Security method


Specifica il livello di sicurezza di un documento come valore numerico.

```cpp
Aspose::Words::Properties::DocumentSecurity Aspose::Words::Properties::BuiltInDocumentProperties::get_Security()
```

## Note


Utilizza questa proprietà solo a scopo informativo perché Microsoft Word non sempre imposta questa proprietà. Questa proprietà è disponibile solo nei documenti DOC e OOXML.

Per proteggere o rimuovere la protezione di un documento usa i metodi [Protect()](../) e [Unprotect](../../../aspose.words/document/unprotect/).

Aspose.Words aggiorna questa proprietà a un valore corretto prima di salvare un documento.

## Esempi



Mostra come utilizzare le proprietà del documento per visualizzare il livello di sicurezza di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// Se configuriamo un documento in sola lettura, visualizzerà questo stato utilizzando la proprietà integrata "Security".
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyRecommended, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// Proteggi da scrittura un documento, quindi verifica il suo livello di sicurezza.
doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyEnforced, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// "Security" è una proprietà descrittiva. Possiamo modificare il suo valore manualmente.
doc = System::MakeObject<Aspose::Words::Document>();

doc->Protect(Aspose::Words::ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")->get_BuiltInDocumentProperties()->get_Security());
```

## Vedi anche

* Enum [DocumentSecurity](../../documentsecurity/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
