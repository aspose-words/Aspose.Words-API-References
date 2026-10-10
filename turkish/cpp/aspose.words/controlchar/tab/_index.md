---
title: "Aspose::Words::ControlChar::Tab yöntemi"
linktitle: "Sekme"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ControlChar::Tab yöntemi. Sekme karakteri: \"\\\\x0009\" veya \"\\\\t\" C++'ta."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/controlchar/tab/
---
## ControlChar::Tab method


Sekme karakteri: "\x0009" veya "\t".

```cpp
static System::String & Aspose::Words::ControlChar::Tab()
```


## Örnekler



Sekme durakları konumları için özel bir aralık ayarlamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Sekme duraklarını her 72 nokta (1 inç) aralıklarla görünür şekilde ayarlayın.
builder->get_Document()->set_DefaultTabStop(72);

// Her sekme karakteri, sonrasındaki metni bir sonraki en yakın sekme durak konumuna çeker.
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::TabChar + u"World!");
```

## Ayrıca Bakınız

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
