---
title: "metodo Aspose::Words::Settings::WriteProtection::SetPassword"
linktitle: "SetPassword"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Settings::WriteProtection::SetPassword. Imposta la password di protezione in scrittura per il documento in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection::SetPassword method


Imposta la password di protezione da scrittura per il documento.

```cpp
void Aspose::Words::Settings::WriteProtection::SetPassword(const System::String &password)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | const System::String\& | La password da impostare. Non può essere **null**, ma può essere una stringa vuota. |
## Note


Se è impostata una password, Microsoft Word richiederà all'utente di inserirla o aprirà il documento in sola lettura.

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
