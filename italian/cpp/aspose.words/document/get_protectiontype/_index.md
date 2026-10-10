---
title: "Metodo Aspose::Words::Document::get_ProtectionType"
linktitle: "get_ProtectionType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_ProtectionType. Restituisce il tipo di protezione del documento attualmente attivo in C++."
type: docs
weight: 44000
url: /it/cpp/aspose.words/document/get_protectiontype/
---
## Document::get_ProtectionType method


Ottiene il tipo di protezione del documento attualmente attivo.

```cpp
Aspose::Words::ProtectionType Aspose::Words::Document::get_ProtectionType()
```

## Note


Questa proprietà consente di recuperare il tipo di protezione del documento attualmente impostato. Per modificare il tipo di protezione del documento, utilizzare i metodi [Protect()](../) e [Unprotect](../unprotect/).

Quando un documento è protetto, l'utente può apportare solo modifiche limitate, come aggiungere annotazioni, effettuare revisioni o compilare un modulo.

Nota che la protezione del documento è diversa dalla protezione di scrittura. La protezione di scrittura è specificata utilizzando [WriteProtection](../get_writeprotection/).

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
