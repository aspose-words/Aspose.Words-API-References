---
title: "Aspose::Words::ControlChar::Cr method"
linktitle: "Cr"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ControlChar::Cr method. Carattere di ritorno a capo: \"\\x000d\" o \"\\r\". Stesso di ParagraphBreak in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/controlchar/cr/
---
## ControlChar::Cr method


Carattere di ritorno a capo: "\x000d" o "\r". Stesso di [ParagraphBreak](../paragraphbreak/).

```cpp
static System::String & Aspose::Words::ControlChar::Cr()
```


## Esempi



Mostra come utilizzare i caratteri di controllo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci paragrafi con testo usando DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Convertire il documento in forma testuale rivela che i caratteri di controllo
// rappresentano alcuni degli elementi strutturali del documento, come le interruzioni di pagina.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Durante la conversione di un documento in forma stringa,
// possiamo omettere alcuni dei caratteri di controllo con il metodo Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Vedi anche

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
