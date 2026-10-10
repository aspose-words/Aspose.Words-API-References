---
title: "Aspose::Words::Fonts::FontSourceBase class"
linktitle: "FontSourceBase"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontSourceBase class. Detta är en abstrakt basklass för de klasser som låter användaren ange olika teckensnittskällor. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class


Detta är en abstrakt basklass för klasserna som låter användaren specificera olika teckensnittskällor. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSourceBase : public Aspose::Fonts::IFontSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Priority](./get_priority/)() const | Returnerar prioriteten för teckensnittskällan. |
| virtual [get_Type](./get_type/)() | Returnerar typen av teckensnittskälla. |
| [get_WarningCallback](./get_warningcallback/)() const | Kallas under bearbetning av teckensnittskällan när ett problem upptäcks som kan leda till förlust av formateringsnoggrannhet. |
| [GetAvailableFonts](./getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via denna källa. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Kallas under bearbetning av teckensnittskällan när ett problem upptäcks som kan leda till förlust av formateringsnoggrannhet. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man använder en typsnittfil i det lokala filsystemet som en typsnittskälla.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Se även

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
