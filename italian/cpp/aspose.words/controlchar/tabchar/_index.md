---
title: "Campo Aspose::Words::ControlChar::TabChar"
linktitle: "TabChar"
second_title: "Riferimento API Aspose.Words per C++"
description: "Campo Aspose::Words::ControlChar::TabChar. Carattere di tabulazione: (char)9 o \"\\t\" in C++."
type: docs
weight: 29000
url: /it/cpp/aspose.words/controlchar/tabchar/
---
## TabChar field


Carattere tabulazione: (char)9 o "\t".

```cpp
static constexpr char16_t Aspose::Words::ControlChar::TabChar
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
