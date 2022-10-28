---
title: FontSourceBase
second_title: Aspose.Words for C++ API Reference
description: This is an abstract base class for the classes that allow the user to specify various font sources.
type: docs
weight: 131
url: /cpp/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class


This is an abstract base class for the classes that allow the user to specify various font sources.

```cpp
class FontSourceBase : public Aspose::Fonts::IFontSource
```

## Methods

| Method | Description |
| --- | --- |
| [get_Priority](./get_priority/)() const | Returns the font source priority. |
| virtual [get_Type](./get_type/)() | Returns the type of the font source. |
| [get_WarningCallback](./get_warningcallback/)() const | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [GetAvailableFonts](./getavailablefonts/)() | Returns list of fonts available via this source. |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter for [Aspose::Words::Fonts::FontSourceBase::get_WarningCallback](./get_warningcallback/). |

## Examples




Shows how to use a font file in the local file system as a font source. 
```cpp
auto fileFontSource = MakeObject<FileFontSource>(MyDir + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = MakeObject<Document>();
doc->set_FontSettings(MakeObject<FontSettings>());
doc->get_FontSettings()->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({fileFontSource}));

ASSERT_EQ(MyDir + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

