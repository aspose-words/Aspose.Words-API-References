---
title: "Aspose::Words::Range::get_Text method"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Range::get_Text metodu. C++'ta aralığın metnini alır."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/range/get_text/
---
## Range::get_Text method


Aralığın metnini alır.

```cpp
System::String Aspose::Words::Range::get_Text()
```

## Açıklamalar


Dönen dize, [ControlChar](../../controlchar/) içinde açıklandığı gibi tüm kontrol ve özel karakterleri içerir.

## Örnekler



Bir aralığın kapsadığı tüm düğümlerin metin içeriğini nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Ayrıca Bakınız

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
