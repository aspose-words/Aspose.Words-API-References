---
title: "Aspose::Words::Document::get_DefaultTabStop metod"
linktitle: "get_DefaultTabStop"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_DefaultTabStop metod. Hämtar eller anger intervallet (i punkter) mellan standardtabbstopp i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words/document/get_defaulttabstop/
---
## Document::get_DefaultTabStop method


Hämtar eller anger intervallet (i punkter) mellan standardtabbstopp.

```cpp
double Aspose::Words::Document::get_DefaultTabStop()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
