---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps metodu"
linktitle: "get_HyphenateCaps"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps metodu. Tüm büyük harflerle yazılmış kelimelerin tirelenip tirelenmeyeceğini belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri C++'da doğrudur."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.settings/hyphenationoptions/get_hyphenatecaps/
---
## HyphenationOptions::get_HyphenateCaps method


Bu özelliği alır veya ayarlar; tüm büyük harflerle yazılmış kelimelerin tirelenip tirelenmeyeceğini belirler. Bu özelliğin varsayılan değeri **true**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps() const
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
