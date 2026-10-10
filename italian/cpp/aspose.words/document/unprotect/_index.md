---
title: "Aspose::Words::Document::Unprotect metodo"
linktitle: "Unprotect"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::Unprotect metodo. Rimuove la protezione dal documento indipendentemente dalla password in C++."
type: docs
weight: 95000
url: /it/cpp/aspose.words/document/unprotect/
---
## Document::Unprotect() method


Rimuove la protezione dal documento indipendentemente dalla password.

```cpp
void Aspose::Words::Document::Unprotect()
```

## Note


Questo metodo rimuove la protezione dal documento anche se ha una password di protezione.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Unprotect(const System::String\&) method


Rimuove la protezione dal documento se viene specificata una password corretta.

```cpp
bool Aspose::Words::Document::Unprotect(const System::String &password)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | const System::String\& | La password con cui rimuovere la protezione del documento. |

### ReturnValue

**true** if a correct password was specified and the document was unprotected.
## Note


Questo metodo rimuove la protezione del documento solo se viene specificata una password corretta.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
