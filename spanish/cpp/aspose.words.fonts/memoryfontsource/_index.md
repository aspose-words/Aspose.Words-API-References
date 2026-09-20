---
title: "Aspose::Words::Fonts::MemoryFontSource class"
linktitle: "MemoryFontSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::MemoryFontSource class. Representa el único archivo de fuente TrueType almacenado en memoria. Para obtener más información, visita el artículo de documentación en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class


Representa el único archivo de fuente TrueType almacenado en memoria. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class MemoryFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | La clave de esta fuente en la caché. |
| [get_FontData](./get_fontdata/)() const | Datos de fuente binarios. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Devuelve la prioridad de la fuente de fuentes. |
| [get_Type](./get_type/)() override | Devuelve el tipo de la fuente de fuentes. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Devuelve la lista de fuentes disponibles a través de esta fuente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&) | Ctor. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t) | Ctor. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) | Ctor. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| static [Type](./type/)() |  |

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

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
