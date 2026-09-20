---
title: "Aspose::Words::Fonts::FileFontSource class"
linktitle: "FileFontSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FileFontSource class. Representa el único archivo de fuente TrueType almacenado en el sistema de archivos. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fonts/filefontsource/
---
## FileFontSource class


Representa el único archivo de fuente TrueType almacenado en el sistema de archivos. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FileFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Métodos

| Método | Descripción |
| --- | --- |
| [FileFontSource](./filefontsource/)(const System::String\&) | Ctor. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t) | Ctor. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t, const System::String\&) | Ctor. |
| [get_CacheKey](./get_cachekey/)() const | La clave de esta fuente en la caché. |
| [get_FilePath](./get_filepath/)() const | Ruta al archivo de fuente. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Devuelve la prioridad de la fuente de fuentes. |
| [get_Type](./get_type/)() override | Devuelve el tipo de la fuente de fuentes. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Devuelve la lista de fuentes disponibles a través de esta fuente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo usar un archivo de fuente en el sistema de archivos local como origen de fuente.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Ver también

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
