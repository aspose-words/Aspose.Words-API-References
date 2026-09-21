---
title: "Aspose::Words::ControlChar::TabChar fält"
linktitle: "TabChar"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ControlChar::TabChar fält. Tabulatortecken: (char)9 eller \"\\t\" i C++."
type: docs
weight: 29000
url: /sv/cpp/aspose.words/controlchar/tabchar/
---
## TabChar field


Tabulatortecken: (char)9 eller "\\t".

```cpp
static constexpr char16_t Aspose::Words::ControlChar::TabChar
```


## Exempel



Visar hur man anger ett anpassat intervall för tabbstopppositioner.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ställ in tabbstopp så att de visas var 72:e punkt (1 tum).
builder->get_Document()->set_DefaultTabStop(72);

// Varje tabulatortecken fäster texten efter det till nästa närmaste tabbstoppposition.
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::TabChar + u"World!");
```

## Se även

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
