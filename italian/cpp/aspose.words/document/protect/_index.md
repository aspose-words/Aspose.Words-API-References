---
title: "Aspose::Words::Document::Protect metodo"
linktitle: "Proteggi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::Protect metodo. Protegge il documento dalle modifiche senza cambiare la password esistente o assegna una password casuale in C++."
type: docs
weight: 67000
url: /it/cpp/aspose.words/document/protect/
---
## Document::Protect(Aspose::Words::ProtectionType) method


Protegge il documento dalle modifiche senza cambiare la password esistente o assegna una password casuale.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tipo | Aspose::Words::ProtectionType | Specifica il tipo di protezione per il documento. |
## Note


Quando un documento è protetto, l'utente può apportare solo modifiche limitate, come aggiungere annotazioni, effettuare revisioni o compilare un modulo.

Quando proteggi un documento e il documento ha già una password di protezione, la password di protezione esistente non viene modificata.

Quando proteggi un documento e il documento non ha una password di protezione, questo metodo assegna una password casuale che rende impossibile rimuovere la protezione del documento in Microsoft Word, ma è comunque possibile rimuovere la protezione del documento in Aspose.Words poiché non richiede una password durante lo sblocco.

## Esempi



Mostra come disattivare la protezione per una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Applica la protezione di scrittura a ogni sezione del documento.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Disattiva la protezione di scrittura per la prima sezione.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// In questo documento di output, saremo in grado di modificare liberamente la prima sezione,
// e potremo modificare solo il contenuto del campo modulo nella seconda sezione.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## Vedi anche

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Protect(Aspose::Words::ProtectionType, const System::String\&) method


Protegge il documento dalle modifiche e opzionalmente imposta una password di protezione.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type, const System::String &password)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tipo | Aspose::Words::ProtectionType | Specifica il tipo di protezione per il documento. |
| password | const System::String\& | La password con cui proteggere il documento. Specifica **null** o una stringa vuota se desideri proteggere il documento senza password. |
## Note


Quando un documento è protetto, l'utente può apportare solo modifiche limitate, come aggiungere annotazioni, effettuare revisioni o compilare un modulo.

Nota che la protezione del documento è diversa dalla protezione di scrittura. La protezione di scrittura è specificata usando il [WriteProtection](../get_writeprotection/).

## Esempi



Mostra come proteggere e rimuovere la protezione di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"password");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// Se apriamo questo documento con Microsoft Word con l'intenzione di modificarlo,
// dovremo inserire la password per superare la protezione.
doc->Save(get_ArtifactsDir() + u"Document.Protect.docx");

// Nota che la protezione si applica solo agli utenti di Microsoft Word che aprono il nostro documento.
// Non abbiamo criptato il documento in alcun modo, e non è necessaria la password per aprirlo e modificarlo programmaticamente.
auto protectedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.Protect.docx");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// Ci sono due modi per rimuovere la protezione da un documento.
// 1 - Senza password:
doc->Unprotect();

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - Con la password corretta:
doc->Unprotect(u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());
```

## Vedi anche

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
