---
title: "Aspose::Words::Fonts::FontSourceBase class"
linktitle: "FontSourceBase"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontSourceBase class. Esta es una clase base abstracta para las clases que permiten al usuario especificar diversas fuentes tipográficas. Para obtener más información, visita el artículo de documentación en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class


Esta es una clase base abstracta para las clases que permiten al usuario especificar diversas fuentes de fuentes. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSourceBase : public Aspose::Fonts::IFontSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Priority](./get_priority/)() const | Devuelve la prioridad de la fuente de fuentes. |
| virtual [get_Type](./get_type/)() | Devuelve el tipo de la fuente de fuentes. |
| [get_WarningCallback](./get_warningcallback/)() const | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| [GetAvailableFonts](./getavailablefonts/)() | Devuelve la lista de fuentes disponibles a través de esta fuente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
