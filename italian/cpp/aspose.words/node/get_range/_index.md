---
title: "Metodo Aspose::Words::Node::get_Range"
linktitle: "get_Range"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Node::get_Range. Restituisce un oggetto Range che rappresenta la porzione di un documento contenuta in questo nodo in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/node/get_range/
---
## Node::get_Range method


Restituisce un oggetto [Range](../../range/) che rappresenta la porzione di un documento contenuta in questo nodo.

```cpp
System::SharedPtr<Aspose::Words::Range> Aspose::Words::Node::get_Range()
```


## Esempi



Mostra come eliminare tutti i nodi da un intervallo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi testo alla prima sezione del documento, quindi aggiungi un'altra sezione.
builder->Write(u"Section 1. ");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Write(u"Section 2.");

ASSERT_EQ(u"Section 1. \fSection 2.", doc->GetText().Trim());

// Rimuovi completamente la prima sezione eliminando tutti i nodi
// all'interno del suo intervallo, inclusa la sezione stessa.
doc->get_Sections()->idx_get(0)->get_Range()->Delete();

ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(u"Section 2.", doc->GetText().Trim());
```

## Vedi anche

* Class [Range](../../range/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
