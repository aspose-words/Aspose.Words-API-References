---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode metodo"
linktitle: "get_LegacyMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode metodo. Ottiene o imposta un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_legacymode/
---
## FindReplaceOptions::get_LegacyMode method


Ottiene o imposta un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode() const
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

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
