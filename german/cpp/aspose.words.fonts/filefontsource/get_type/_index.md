---
title: "Aspose::Words::Fonts::FileFontSource::get_Type Methode"
linktitle: "get_Type"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FileFontSource::get_Type Methode. Gibt den Typ der Schriftquellen in C++ zurück."
type: docs
weight: 5000
url: /de/cpp/aspose.words.fonts/filefontsource/get_type/
---
## FileFontSource::get_Type method


Gibt den Typ der Schriftquelle zurück.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FileFontSource::get_Type() override
```


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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
