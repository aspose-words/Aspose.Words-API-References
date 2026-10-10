---
title: "Aspose::Words::TabStopCollection::GetIndexByPosition method"
linktitle: "GetIndexByPosition"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TabStopCollection::GetIndexByPosition method. Ottiene l'indice di una tabulazione con la posizione specificata in punti in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection::GetIndexByPosition method


Restituisce l'indice di una tabulazione con la posizione specificata in punti.

```cpp
int32_t Aspose::Words::TabStopCollection::GetIndexByPosition(double position)
```


## Esempi



Mostra come cercare una posizione per verificare se esiste una tabulazione e ottenere il suo indice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

// Aggiungi una tabulazione a una posizione di 30 mm.
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Un risultato di "0" restituito da "GetIndexByPosition" conferma che una tabulazione
// a 30 mm esiste in questa raccolta, ed è all'indice 0.
ASSERT_EQ(0, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(30)));

// Un "-1" restituito da "GetIndexByPosition" conferma che
// non esiste alcuna tabulazione in questa raccolta con una posizione di 60 mm.
ASSERT_EQ(-1, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(60)));
```

## Vedi anche

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
