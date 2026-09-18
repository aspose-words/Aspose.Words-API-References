---
title: "Aspose::Words::Fonts::FileFontSource class"
linktitle: "FileFontSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FileFontSource class. Stellt die einzelne TrueType‑Schriftdatei dar, die im Dateisystem gespeichert ist. Weitere Informationen finden Sie im Dokumentationsartikel zu C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fonts/filefontsource/
---
## FileFontSource class


Stellt die einzelne TrueType‑Schriftdatei dar, die im Dateisystem gespeichert ist. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FileFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [FileFontSource](./filefontsource/)(const System::String\&) | Konstruktor. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t) | Konstruktor. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t, const System::String\&) | Konstruktor. |
| [get_CacheKey](./get_cachekey/)() const | Der Schlüssel dieser Quelle im Cache. |
| [get_FilePath](./get_filepath/)() const | Pfad zur Schriftdatei. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Gibt die Priorität der Schriftquellen zurück. |
| [get_Type](./get_type/)() override | Gibt den Typ der Schriftquelle zurück. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungsgenauigkeit führen könnte. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Gibt eine Liste der über diese Quelle verfügbaren Schriften zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungsgenauigkeit führen könnte. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man eine Schriftdatei im lokalen Dateisystem als Schriftquelle verwendet.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Siehe auch

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
