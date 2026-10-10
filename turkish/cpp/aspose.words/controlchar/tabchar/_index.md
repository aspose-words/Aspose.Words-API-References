---
title: "Aspose::Words::ControlChar::TabChar alanı"
linktitle: "TabChar"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ControlChar::TabChar alanı. Sekme karakteri: (char)9 veya \"\\t\" C++'da."
type: docs
weight: 29000
url: /tr/cpp/aspose.words/controlchar/tabchar/
---
## TabChar field


Sekme karakteri: (char)9 veya "\t".

```cpp
static constexpr char16_t Aspose::Words::ControlChar::TabChar
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
