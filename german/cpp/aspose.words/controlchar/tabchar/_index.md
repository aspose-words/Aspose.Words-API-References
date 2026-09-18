---
title: "Aspose::Words::ControlChar::TabChar Feld"
linktitle: "TabChar"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ControlChar::TabChar Feld. Tabulatorzeichen: (char)9 oder \"\\t\" in C++."
type: docs
weight: 29000
url: /de/cpp/aspose.words/controlchar/tabchar/
---
## TabChar field


Tabulatorzeichen: (char)9 oder "\t".

```cpp
static constexpr char16_t Aspose::Words::ControlChar::TabChar
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

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
