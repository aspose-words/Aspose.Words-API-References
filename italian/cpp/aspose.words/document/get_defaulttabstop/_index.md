---
title: "Aspose::Words::Document::get_DefaultTabStop metodo"
linktitle: "get_DefaultTabStop"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_DefaultTabStop metodo. Ottiene o imposta l'intervallo (in punti) tra le tabulazioni predefinite in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words/document/get_defaulttabstop/
---
## Document::get_DefaultTabStop method


Ottiene o imposta l'intervallo (in punti) tra le tabulazioni predefinite.

```cpp
double Aspose::Words::Document::get_DefaultTabStop()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
