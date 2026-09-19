---
title: "Aspose::Words::Range::get_Text metodo"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Range::get_Text metodo. Ottiene il testo dell'intervallo in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/range/get_text/
---
## Range::get_Text method


Ottiene il testo dell'intervallo.

```cpp
System::String Aspose::Words::Range::get_Text()
```

## Note


La stringa restituita include tutti i caratteri di controllo e speciali come descritti in [ControlChar](../../controlchar/).

## Esempi



Mostra come ottenere il contenuto testuale di tutti i nodi coperti da un intervallo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Vedi anche

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
