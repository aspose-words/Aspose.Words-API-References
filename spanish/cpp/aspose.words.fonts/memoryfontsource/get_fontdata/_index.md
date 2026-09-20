---
title: "Aspose::Words::Fonts::MemoryFontSource::get_FontData método"
linktitle: "get_FontData"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::MemoryFontSource::get_FontData método. Datos binarios de fuente en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.fonts/memoryfontsource/get_fontdata/
---
## MemoryFontSource::get_FontData method


Datos de fuente binarios.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::MemoryFontSource::get_FontData() const
```


## Ejemplos



Muestra cómo usar una matriz de bytes con datos de un archivo de fuente como una fuente.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Ver también

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
