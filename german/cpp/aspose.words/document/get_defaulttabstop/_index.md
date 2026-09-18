---
title: "Aspose::Words::Document::get_DefaultTabStop Methode"
linktitle: "get_DefaultTabStop"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_DefaultTabStop Methode. Liest oder setzt das Intervall (in Punkten) zwischen den Standard-Tabstopps in C++."
type: docs
weight: 20000
url: /de/cpp/aspose.words/document/get_defaulttabstop/
---
## Document::get_DefaultTabStop method


Liest oder legt das Intervall (in Punkten) zwischen den Standard-Tabulatoren fest.

```cpp
double Aspose::Words::Document::get_DefaultTabStop()
```


## Beispiele



Zeigt, wie man ein benutzerdefiniertes Intervall für Tabstopp-Positionen festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Setzt Tabstopps so, dass sie alle 72 Punkte (1 Zoll) erscheinen.
builder->get_Document()->set_DefaultTabStop(72);

// Jedes Tabulatorzeichen richtet den nachfolgenden Text an der nächstgelegenen Tabstopp-Position aus.
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::TabChar + u"World!");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
