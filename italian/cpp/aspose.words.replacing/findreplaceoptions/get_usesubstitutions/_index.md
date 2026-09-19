---
title: "Metodo Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions"
linktitle: "get_UseSubstitutions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions. Ottiene o imposta un valore booleano che indica se riconoscere e utilizzare le sostituzioni nei modelli di sostituzione. Il valore predefinito è false in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_usesubstitutions/
---
## FindReplaceOptions::get_UseSubstitutions method


Ottiene o imposta un valore booleano che indica se riconoscere e utilizzare le sostituzioni nei modelli di sostituzione. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions() const
```


## Esempi



Mostra come riconoscere e utilizzare le sostituzioni nei modelli di sostituzione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// L'utilizzo della modalità legacy non supporta molte funzionalità avanzate, quindi è necessario impostarla su 'false'.
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```


Mostra come sostituire il testo con le sostituzioni.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"John sold a car to Paul.");
builder->Writeln(u"Jane sold a house to Joe.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta la proprietà "UseSubstitutions" su "true" per ottenere
// l'operazione di ricerca e sostituzione per riconoscere gli elementi di sostituzione.
// Imposta la proprietà "UseSubstitutions" su "false" per ignorare gli elementi di sostituzione.
options->set_UseSubstitutions(useSubstitutions);

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc->get_Range()->Replace(regex, u"$3 bought a $2 from $1", options);

ASSERT_EQ(useSubstitutions ? System::String(u"Paul bought a car from John.\rJoe bought a house from Jane.") : System::String(u"$3 bought a $2 from $1.\r$3 bought a $2 from $1."), doc->GetText().Trim());
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
