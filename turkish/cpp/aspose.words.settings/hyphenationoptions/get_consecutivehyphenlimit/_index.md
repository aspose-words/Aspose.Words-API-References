---
title: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit metodu"
linktitle: "get_ConsecutiveHyphenLimit"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit metodu. Tire ile biten ardışık satırların maksimum sayısını alır veya ayarlar. Bu özelliğin varsayılan değeri C++'da 0'dır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.settings/hyphenationoptions/get_consecutivehyphenlimit/
---
## HyphenationOptions::get_ConsecutiveHyphenLimit method


Bu özelliği alır veya ayarlar; tire ile sonlandırılabilecek ardışık satırların azami sayısını belirler. Bu özelliğin varsayılan değeri 0'dır.

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit() const
```

## Açıklamalar


Bu özelliğin değeri 0 olarak ayarlanırsa, tire ile biten herhangi sayıda ardışık satır olabilir.

Bu özellik, PDF gibi sabit sayfa formatlarına kaydedilirken etkili değildir.

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
