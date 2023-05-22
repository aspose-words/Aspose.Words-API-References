---
title: Aspose::Words::Fonts::MemoryFontSource class
linktitle: MemoryFontSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::MemoryFontSource class. Represents the single TrueType font file stored in memory. To learn more, visit the  documentation article in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class


Represents the single TrueType font file stored in memory. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class MemoryFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Methods

| Method | Description |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | The key of this source in the cache. |
| [get_FontData](./get_fontdata/)() const | Binary font data. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Returns the font source priority. |
| [get_Type](./get_type/)() override | Returns the type of the font source. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Returns list of fonts available via this source. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&) | Ctor. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t) | Ctor. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) | Ctor. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter for [Aspose::Words::Fonts::FontSourceBase::get_WarningCallback](../fontsourcebase/get_warningcallback/). |
| static [Type](./type/)() |  |

## Examples



Shows how to use a byte array with data from a font file as a font source. 
```cpp
ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(MyDir + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = MakeObject<MemoryFontSource>(fontBytes, 0);

auto doc = MakeObject<Document>();
doc->set_FontSettings(MakeObject<FontSettings>());
doc->get_FontSettings()->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## See Also

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
