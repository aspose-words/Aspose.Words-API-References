---
title: "Aspose::Words::Fonts::MemoryFontSource Klasse"
linktitle: "MemoryFontSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::MemoryFontSource Klasse. Stellt die einzelne TrueType-Schriftdatei dar, die im Speicher abgelegt ist. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class


Stellt die einzelne TrueType-Schriftdatei dar, die im Speicher gespeichert ist. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class MemoryFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | Der Schlüssel dieser Quelle im Cache. |
| [get_FontData](./get_fontdata/)() const | Binäre Schriftartdaten. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Gibt die Priorität der Schriftquellen zurück. |
| [get_Type](./get_type/)() override | Gibt den Typ der Schriftquelle zurück. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungsgenauigkeit führen könnte. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Gibt eine Liste der über diese Quelle verfügbaren Schriften zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&) | Konstruktor. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t) | Konstruktor. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) | Konstruktor. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungsgenauigkeit führen könnte. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man ein Byte-Array mit Daten aus einer Schriftdatei als Schriftquelle verwendet.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Siehe auch

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
