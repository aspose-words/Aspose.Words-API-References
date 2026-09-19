---
title: "Metodo Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted"
linktitle: "get_IgnoreDeleted"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted. Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno delle revisioni di cancellazione. Il valore predefinito è false in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_ignoredeleted/
---
## FindReplaceOptions::get_IgnoreDeleted method


Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno delle revisioni di eliminazione. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted() const
```


## Esempi



Mostra come includere o ignorare il testo all'interno delle revisioni di cancellazione durante un'operazione di ricerca e sostituzione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Inizia a tenere traccia delle revisioni e rimuovi il secondo paragrafo, il quale creerà una revisione di cancellazione.
// Quel paragrafo rimarrà nel documento finché non accetteremo la revisione di cancellazione.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->Remove();
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsDeleteRevision());

// Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta il flag "IgnoreDeleted" su "true" per ottenere la ricerca e sostituzione
// operazione per ignorare i paragrafi che sono revisioni di cancellazione.
// Imposta il flag "IgnoreDeleted" su "false" per ottenere la ricerca e sostituzione
// operazione per cercare anche il testo all'interno delle revisioni di cancellazione.
options->set_IgnoreDeleted(ignoreTextInsideDeleteRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideDeleteRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
