---
title: Aspose::Words::Fonts::FontSourceBase class
linktitle: FontSourceBase
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontSourceBase class. This is an abstract base class for the classes that allow the user to specify various font sources. To learn more, visit the  documentation article in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class


This is an abstract base class for the classes that allow the user to specify various font sources. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

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
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
