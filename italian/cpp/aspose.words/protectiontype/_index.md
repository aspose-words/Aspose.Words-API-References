---
title: "Enum Aspose::Words::ProtectionType"
linktitle: "ProtectionType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::ProtectionType. Tipo di protezione per un documento in C++."
type: docs
weight: 111000
url: /it/cpp/aspose.words/protectiontype/
---
## ProtectionType enum


Tipo di protezione per un documento.

```cpp
enum class ProtectionType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AllowOnlyComments | 1 | L'utente può modificare solo i commenti nel documento. |
| AllowOnlyFormFields | 2 | L'utente può inserire dati solo nei campi modulo del documento. |
| AllowOnlyRevisions | 0 | L'utente può aggiungere solo segni di revisione al documento. |
| ReadOnly | 3 | Non sono consentite modifiche al documento. Disponibile da Microsoft Word 2003. |
| NoProtection | -1 | Il documento non è protetto. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
