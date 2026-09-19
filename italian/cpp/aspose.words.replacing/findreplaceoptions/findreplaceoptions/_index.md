---
title: "Costruttore Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions. Inizializza una nuova istanza della classe FindReplaceOptions con le impostazioni predefinite in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions::FindReplaceOptions() constructor


Inizializza una nuova istanza della classe [FindReplaceOptions](../) con le impostazioni predefinite.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions()
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
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection) constructor


Inizializza una nuova istanza della classe [FindReplaceOptions](../) con la direzione specificata.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| direzione | Aspose::Words::Replacing::FindReplaceDirection | La direzione dell'operazione di ricerca e sostituzione. |

## Vedi anche

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Inizializza una nuova istanza della classe [FindReplaceOptions](../) con la direzione specificata e la callback di sostituzione.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction, const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| direzione | Aspose::Words::Replacing::FindReplaceDirection | La direzione dell'operazione di ricerca e sostituzione. |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | La callback da utilizzare per sostituire il testo trovato. |

## Vedi anche

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


Inizializza una nuova istanza della classe [FindReplaceOptions](../) con la callback di sostituzione specificata.

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | La callback da utilizzare per sostituire il testo trovato. |

## Vedi anche

* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
