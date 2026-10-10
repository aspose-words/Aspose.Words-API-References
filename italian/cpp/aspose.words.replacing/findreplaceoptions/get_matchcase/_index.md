---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase metodo"
linktitle: "get_MatchCase"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase metodo. True indica un confronto sensibile al maiuscolo/minuscolo, false indica un confronto non sensibile al maiuscolo/minuscolo in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_matchcase/
---
## FindReplaceOptions::get_MatchCase method


True indica un confronto sensibile al maiuscolo/minuscolo, false indica un confronto non sensibile al maiuscolo/minuscolo.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase() const
```


## Esempi



Mostra come attivare/disattivare la sensibilità al maiuscolo/minuscolo durante un'operazione di ricerca e sostituzione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta il flag "MatchCase" su "true" per applicare la sensibilità al maiuscolo/minuscolo durante la ricerca delle stringhe da sostituire.
// Imposta il flag "MatchCase" su "false" per ignorare le differenze di maiuscole/minuscole durante la ricerca del testo da sostituire.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
