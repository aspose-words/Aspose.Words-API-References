---
title: "Metodo get_Type di Aspose::Words::Fonts::MemoryFontSource"
linktitle: "get_Type"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_Type di Aspose::Words::Fonts::MemoryFontSource. Restituisce il tipo della sorgente del font in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fonts/memoryfontsource/get_type/
---
## MemoryFontSource::get_Type method


Restituisce il tipo della sorgente del font.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::MemoryFontSource::get_Type() override
```


## Esempi



Mostra come utilizzare un array di byte con i dati di un file di carattere come sorgente di caratteri.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Vedi anche

* Enum [FontSourceType](../../fontsourcetype/)
* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
