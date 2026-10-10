---
title: "Aspose::Words::Comparing::Granularity enum"
linktitle: "Granularity"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Comparing::Granularity enum. Specifica la granularità delle modifiche da tenere traccia durante il confronto di due documenti in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.comparing/granularity/
---
## Granularity enum


Specifica la granularità delle modifiche da tenere traccia durante il confronto di due documenti.

```cpp
enum class Granularity
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| CharLevel | 0 | Specifica le modifiche a livello di carattere. |
| WordLevel | 1 | Specifica le modifiche a livello di parola. |


## Esempi



Mostra come specificare una granularità durante il confronto dei documenti.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Specifica se le modifiche sono tracciate
// per carattere ('Granularity.CharLevel'), o per parola ('Granularity.WordLevel').
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// La raccolta di gruppi di revisione del primo documento contiene tutte le differenze tra i documenti.
System::SharedPtr<Aspose::Words::RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## Vedi anche

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
