---
title: "Aspose::Words::Section::get_ProtectedForForms metodo"
linktitle: "get_ProtectedForForms"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Section::get_ProtectedForForms metodo. Vero se la sezione è protetta per i moduli. Quando una sezione è protetta per i moduli, gli utenti possono selezionare e modificare il testo solo nei campi modulo in Microsoft Word in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words/section/get_protectedforforms/
---
## Section::get_ProtectedForForms method


Vero se la sezione è protetta per i moduli. Quando una sezione è protetta per i moduli, gli utenti possono selezionare e modificare il testo solo nei campi modulo in Microsoft Word.

```cpp
bool Aspose::Words::Section::get_ProtectedForForms()
```


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

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
