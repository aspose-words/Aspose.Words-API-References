---
title: "Aspose::Words::Document::get_DefaultTabStop yöntemi"
linktitle: "get_DefaultTabStop"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_DefaultTabStop yöntemi. C++'ta varsayılan sekme durakları arasındaki aralığı (nokta cinsinden) alır veya ayarlar."
type: docs
weight: 20000
url: /tr/cpp/aspose.words/document/get_defaulttabstop/
---
## Document::get_DefaultTabStop method


Varsayılan sekme durakları arasındaki aralığı (puan cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::Document::get_DefaultTabStop()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
