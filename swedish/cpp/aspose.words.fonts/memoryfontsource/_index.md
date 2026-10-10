---
title: "Aspose::Words::Fonts::MemoryFontSource class"
linktitle: "MemoryFontSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::MemoryFontSource class. Representerar den enda TrueType-teckensnittsfilen som lagras i minnet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class


Representerar den enda TrueType-teckensnittsfilen som lagras i minnet. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class MemoryFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | Nyckeln för denna källa i cachen. |
| [get_FontData](./get_fontdata/)() const | Binär teckensnittsdata. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Returnerar prioriteten för teckensnittskällan. |
| [get_Type](./get_type/)() override | Returnerar typen av teckensnittskälla. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Kallas under bearbetning av teckensnittskällan när ett problem upptäcks som kan leda till förlust av formateringsnoggrannhet. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via denna källa. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&) | Konstruktör. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t) | Konstruktör. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) | Konstruktör. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Kallas under bearbetning av teckensnittskällan när ett problem upptäcks som kan leda till förlust av formateringsnoggrannhet. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man använder en bytearray med data från en teckensnittfil som en teckensnittskälla.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Se även

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
