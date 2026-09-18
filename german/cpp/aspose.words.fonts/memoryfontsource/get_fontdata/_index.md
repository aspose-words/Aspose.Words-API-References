---
title: "Aspose::Words::Fonts::MemoryFontSource::get_FontData Methode"
linktitle: "get_FontData"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::MemoryFontSource::get_FontData Methode. Binäre Schriftartdaten in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.fonts/memoryfontsource/get_fontdata/
---
## MemoryFontSource::get_FontData method


Binäre Schriftartdaten.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::MemoryFontSource::get_FontData() const
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

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
