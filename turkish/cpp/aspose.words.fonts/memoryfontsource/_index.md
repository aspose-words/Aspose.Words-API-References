---
title: "Aspose::Words::Fonts::MemoryFontSource sınıfı"
linktitle: "MemoryFontSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::MemoryFontSource sınıfı. Bellekte depolanan tek bir TrueType yazı tipi dosyasını temsil eder. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class


Bellekte depolanan tek bir TrueType yazı tipi dosyasını temsil eder. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class MemoryFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | Bu kaynağın önbellekteki anahtarı. |
| [get_FontData](./get_fontdata/)() const | İkili yazı tipi verileri. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Yazı tipi kaynağı önceliğini döndürür. |
| [get_Type](./get_type/)() override | Yazı tipi kaynağının türünü döndürür. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Biçimlendirme doğruluğu kaybına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Bu kaynak üzerinden kullanılabilir yazı tiplerinin listesini döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&) | Yapıcı. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t) | Yapıcı. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) | Yapıcı. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Biçimlendirme doğruluğu kaybına neden olabilecek bir sorun tespit edildiğinde, yazı tipi kaynağının işlenmesi sırasında çağrılır. |
| static [Type](./type/)() |  |

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

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
