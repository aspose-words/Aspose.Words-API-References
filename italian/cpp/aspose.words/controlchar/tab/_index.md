---
title: "Aspose::Words::ControlChar::Tab metodo"
linktitle: "Tab"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ControlChar::Tab metodo. Carattere di tabulazione: \"\\x0009\" o \"\\t\" in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/controlchar/tab/
---
## ControlChar::Tab method


Carattere di tabulazione: "\x0009" o "\t".

```cpp
static System::String & Aspose::Words::ControlChar::Tab()
```


## Esempi



Mostra come impostare un intervallo personalizzato per le posizioni delle tabulazioni.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta le tabulazioni per apparire ogni 72 punti (1 pollice).
builder->get_Document()->set_DefaultTabStop(72);

// Ogni carattere di tabulazione aggancia il testo successivo alla posizione della tabulazione più vicina.
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::TabChar + u"World!");
```

## Vedi anche

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
