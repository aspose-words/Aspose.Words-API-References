---
title: "Aspose::Words::Fonts::MemoryFontSource::get_Type Methode"
linktitle: "get_Type"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::MemoryFontSource::get_Type Methode. Gibt den Typ der Schriftquelle in C++ zurück."
type: docs
weight: 5000
url: /de/cpp/aspose.words.fonts/memoryfontsource/get_type/
---
## MemoryFontSource::get_Type method


Gibt den Typ der Schriftquelle zurück.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::MemoryFontSource::get_Type() override
```


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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
