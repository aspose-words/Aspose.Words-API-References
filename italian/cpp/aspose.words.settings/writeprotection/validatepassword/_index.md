---
title: "metodo Aspose::Words::Settings::WriteProtection::ValidatePassword"
linktitle: "ValidatePassword"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Settings::WriteProtection::ValidatePassword. Restituisce true se la password specificata è la stessa della password di protezione in scrittura con cui il documento è stato protetto. Se il documento non è protetto in scrittura con password, restituisce false in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection::ValidatePassword method


Restituisce **true** se la password specificata è la stessa della password di protezione da scrittura con cui il documento è stato protetto. Se il documento non è protetto da scrittura con password, restituisce **false**.

```cpp
bool Aspose::Words::Settings::WriteProtection::ValidatePassword(const System::String &password)
```


## Esempi



Mostra come proteggere un documento con una password.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// Inserisci una password di lunghezza fino a 15 caratteri, quindi verifica lo stato di protezione del documento.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// La protezione non impedisce che il documento venga modificato programmaticamente, né cifra il contenuto.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## Vedi anche

* Class [WriteProtection](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
