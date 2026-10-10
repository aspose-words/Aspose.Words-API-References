---
title: "Aspose::Words::Settings::WriteProtection classe"
linktitle: "WriteProtection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Settings::WriteProtection classe. Specifica le impostazioni di protezione da scrittura per un documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.settings/writeprotection/
---
## WriteProtection class


Specifica le impostazioni di protezione in scrittura per un documento. Per saperne di più, visita l'articolo di documentazione [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class WriteProtection : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_IsWriteProtected](./get_iswriteprotected/)() | Restituisce **true** quando è impostata una password di protezione da scrittura. |
| [get_ReadOnlyRecommended](./get_readonlyrecommended/)() const | Specifica se l'autore del documento ha raccomandato che il documento venga aperto in sola lettura. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ReadOnlyRecommended](./set_readonlyrecommended/)(bool) | Impostatore per [Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended](./get_readonlyrecommended/). |
| [SetPassword](./setpassword/)(const System::String\&) | Imposta la password di protezione da scrittura per il documento. |
| static [Type](./type/)() |  |
| [ValidatePassword](./validatepassword/)(const System::String\&) | Restituisce **true** se la password specificata è la stessa della password di protezione da scrittura con cui il documento è stato protetto. Se il documento non è protetto da scrittura con password, restituisce **false**. |
## Note


La protezione da scrittura specifica se l'autore ha raccomandato che il documento debba essere aperto in sola lettura e/o richieda una password per modificare un documento.

La protezione dalla scrittura è diversa dalla protezione del documento. La protezione dalla scrittura è specificata in Microsoft Word nelle opzioni della finestra di dialogo Salva con nome.

Non si creano istanze di questa classe direttamente. Si accede alle impostazioni di protezione del documento tramite la proprietà [WriteProtection](../../aspose.words/document/get_writeprotection/).

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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
