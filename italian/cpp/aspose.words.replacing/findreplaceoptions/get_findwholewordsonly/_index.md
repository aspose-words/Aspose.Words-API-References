---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly metodo"
linktitle: "get_FindWholeWordsOnly"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly metodo. True indica che oldValue deve essere una parola autonoma in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_findwholewordsonly/
---
## FindReplaceOptions::get_FindWholeWordsOnly method


True indica che oldValue deve essere una parola autonoma.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly() const
```


## Esempi



Mostra come attivare/disattivare le operazioni di ricerca e sostituzione limitate a parole isolate.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta il flag "FindWholeWordsOnly" su "true" per sostituire il testo trovato se non fa parte di un'altra parola.
// Imposta il flag "FindWholeWordsOnly" su "false" per sostituire tutto il testo indipendentemente dal contesto.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
