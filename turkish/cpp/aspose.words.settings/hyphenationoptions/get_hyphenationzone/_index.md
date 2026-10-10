---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone metodu"
linktitle: "get_HyphenationZone"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone metodu. Sağ kenar boşluğundan 1/20 puan biriminde, kelimeleri hecelemediğiniz mesafeyi alır veya ayarlar. Bu özelliğin varsayılan değeri C++'ta 360 (0.25 inç) dir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.settings/hyphenationoptions/get_hyphenationzone/
---
## HyphenationOptions::get_HyphenationZone method


Bu özelliği alır veya ayarlar; sağ kenardan 1/20 puan biriminde, kelimeleri tirelemek istemediğiniz mesafeyi belirler. Bu özelliğin varsayılan değeri 360 (0.25 inç)dır.

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone() const
```


## Örnekler



Otomatik tirelemeyi nasıl yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## Ayrıca Bakınız

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
