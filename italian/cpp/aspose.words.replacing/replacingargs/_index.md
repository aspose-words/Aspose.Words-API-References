---
title: "Classe Aspose::Words::Replacing::ReplacingArgs"
linktitle: "ReplacingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::ReplacingArgs class. Fornisce dati per un'operazione di sostituzione personalizzata. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class


Fornisce dati per un'operazione di sostituzione personalizzata. Per saperne di più, visita l'articolo di documentazione [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/).

```cpp
class ReplacingArgs : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_GroupIndex](./get_groupindex/)() const | Identifica, per indice, un gruppo catturato nel [Match](./get_match/) che deve essere sostituito con la stringa di [Replacement](./get_replacement/). |
| [get_GroupName](./get_groupname/)() const | Identifica, per nome, un gruppo catturato nel [Match](./get_match/) che deve essere sostituito con la stringa di [Replacement](./get_replacement/). |
| [get_Match](./get_match/)() const | Il **Match** risultante da una singola corrispondenza di espressione regolare durante un **Replace**. |
| [get_MatchEndNode](./get_matchendnode/)() const | Restituisce il nodo che contiene la fine della corrispondenza. |
| [get_MatchNode](./get_matchnode/)() const | Restituisce il nodo che contiene l'inizio della corrispondenza. |
| [get_MatchOffset](./get_matchoffset/)() const | Restituisce la posizione di partenza a indice zero della corrispondenza a partire dall'inizio del nodo che contiene l'inizio della corrispondenza. |
| [get_Replacement](./get_replacement/)() const | Restituisce la stringa di sostituzione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GroupIndex](./set_groupindex/)(int32_t) | Setter per [Aspose::Words::Replacing::ReplacingArgs::get_GroupIndex](./get_groupindex/). |
| [set_GroupName](./set_groupname/)(const System::String\&) | Setter per [Aspose::Words::Replacing::ReplacingArgs::get_GroupName](./get_groupname/). |
| [set_Replacement](./set_replacement/)(const System::String\&) | Imposta la stringa di sostituzione. |
| static [Type](./type/)() |  |

## Vedi anche

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
