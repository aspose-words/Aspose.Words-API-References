---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted metodo"
linktitle: "get_IgnoreInserted"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted metodo. Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno delle revisioni di inserimento. Il valore predefinito è false in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreinserted/
---
## FindReplaceOptions::get_IgnoreInserted method


Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno delle revisioni di inserimento. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted() const
```


## Esempi



Mostra come includere o ignorare il testo all'interno delle revisioni di inserimento durante un'operazione di trova-e-sostituisci.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

// Inizia a tenere traccia delle revisioni e inserisci un paragrafo. Quel paragrafo sarà una revisione di inserimento.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"Hello again!");
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsInsertRevision());

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta il flag "IgnoreInserted" su "true" per ottenere il trova-e-sostituisci
// operazione per ignorare i paragrafi che sono revisioni di inserimento.
// Imposta il flag "IgnoreInserted" su "false" per ottenere il trova-e-sostituisci
// operazione per cercare anche il testo all'interno delle revisioni di inserimento.
options->set_IgnoreInserted(ignoreTextInsideInsertRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideInsertRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
