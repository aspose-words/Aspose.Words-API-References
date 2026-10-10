---
title: "Aspose::Words::Properties::DocumentSecurity enum"
linktitle: "DocumentSecurity"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::DocumentSecurity enum. Utilizzato come valore per la proprietà Security. Specifica il livello di sicurezza di un documento come valore numerico in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enum


Utilizzato come valore per la proprietà [Security](../builtindocumentproperties/get_security/). Specifica il livello di sicurezza di un documento come valore numerico.

```cpp
enum class DocumentSecurity
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Non ci sono stati di sicurezza specificati dalla proprietà. |
| PasswordProtected | 1 | Il documento è protetto da password. (Nota: non è mai stato riscontrato in un documento finora). |
| ReadOnlyRecommended | 2 | Il documento da aprire in sola lettura se possibile, ma l'impostazione può essere sovrascritta. |
| ReadOnlyEnforced | 4 | Il documento da aprire sempre in sola lettura. |
| ReadOnlyExceptAnnotations | 8 | Il documento da aprire sempre in sola lettura, eccetto per le annotazioni. |


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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
