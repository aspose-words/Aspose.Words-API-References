---
title: "Aspose::Words::Range::Delete metodo"
linktitle: "Elimina"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Range::Delete metodo. Elimina tutti i caratteri dell'intervallo in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/range/delete/
---
## Range::Delete method


Elimina tutti i caratteri dell'intervallo.

```cpp
void Aspose::Words::Range::Delete()
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

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
