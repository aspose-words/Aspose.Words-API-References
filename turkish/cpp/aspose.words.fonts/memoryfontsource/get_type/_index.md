---
title: "Aspose::Words::Fonts::MemoryFontSource::get_Type method"
linktitle: "get_Type"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::MemoryFontSource::get_Type method. C++'ta yazı tipi kaynağının tipini döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fonts/memoryfontsource/get_type/
---
## MemoryFontSource::get_Type method


Yazı tipi kaynağının türünü döndürür.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::MemoryFontSource::get_Type() override
```


## Örnekler



Bir yazı tipi dosyasından gelen verilerle bir bayt dizisini yazı tipi kaynağı olarak nasıl kullanacağınızı gösterir.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Ayrıca Bakınız

* Enum [FontSourceType](../../fontsourcetype/)
* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
