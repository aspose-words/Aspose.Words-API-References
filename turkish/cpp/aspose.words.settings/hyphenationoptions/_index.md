---
title: "Aspose::Words::Settings::HyphenationOptions sınıfı"
linktitle: "HyphenationOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::HyphenationOptions sınıfı. Belge heceleme seçeneklerini yapılandırmaya olanak tanır. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class


Belge hecelemesi seçeneklerini yapılandırmaya izin verir. Daha fazla bilgi için, [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/) dokümantasyon makalesini ziyaret edin.

```cpp
class HyphenationOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AutoHyphenation](./get_autohyphenation/)() const | Belge için otomatik hecelemenin açık olup olmadığını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri **false**. |
| [get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)() const | Bu özelliği alır veya ayarlar; tire ile sonlandırılabilecek ardışık satırların azami sayısını belirler. Bu özelliğin varsayılan değeri 0'dır. |
| [get_HyphenateCaps](./get_hyphenatecaps/)() const | Bu özelliği alır veya ayarlar; tüm büyük harflerle yazılmış kelimelerin tirelenip tirelenmeyeceğini belirler. Bu özelliğin varsayılan değeri **true**. |
| [get_HyphenationZone](./get_hyphenationzone/)() const | Bu özelliği alır veya ayarlar; sağ kenardan 1/20 puan biriminde, kelimeleri tirelemek istemediğiniz mesafeyi belirler. Bu özelliğin varsayılan değeri 360 (0.25 inç)dır. |
| [GetType](./gettype/)() const override |  |
| [HyphenationOptions](./hyphenationoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AutoHyphenation](./set_autohyphenation/)(bool) | Ayarlayıcı: [Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation](./get_autohyphenation/). |
| [set_ConsecutiveHyphenLimit](./set_consecutivehyphenlimit/)(int32_t) | Ayarlayıcı: [Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/). |
| [set_HyphenateCaps](./set_hyphenatecaps/)(bool) | Ayarlayıcı: [Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps](./get_hyphenatecaps/). |
| [set_HyphenationZone](./set_hyphenationzone/)(int32_t) | Ayarlayıcı: [Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone](./get_hyphenationzone/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
