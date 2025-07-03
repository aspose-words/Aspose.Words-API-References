---
title: Aspose::Words::Fonts::FileFontSource class
linktitle: FileFontSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FileFontSource class. Represents the single TrueType font file stored in the file system. To learn more, visit the  documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fonts/filefontsource/
---
## FileFontSource class


Represents the single TrueType font file stored in the file system. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FileFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Methods

| Method | Description |
| --- | --- |
| [FileFontSource](./filefontsource/)(const System::String\&) | Ctor. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t) | Ctor. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t, const System::String\&) | Ctor. |
| [get_CacheKey](./get_cachekey/)() const | The key of this source in the cache. |
| [get_FilePath](./get_filepath/)() const | Path to the font file. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Returns the font source priority. |
| [get_Type](./get_type/)() override | Returns the type of the font source. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Returns list of fonts available via this source. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| static [Type](./type/)() |  |

## Examples



Shows how to use a font file in the local file system as a font source. 
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## See Also

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
