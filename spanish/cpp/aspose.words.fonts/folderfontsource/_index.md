---
title: "Aspose::Words::Fonts::FolderFontSource clase"
linktitle: "FolderFontSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FolderFontSource clase. Representa la carpeta que contiene archivos de fuentes TrueType. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


Representa la carpeta que contiene archivos de fuentes TrueType. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FolderFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Métodos

| Método | Descripción |
| --- | --- |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool) | Ctor. |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool, int32_t) | Ctor. |
| [get_FolderPath](./get_folderpath/)() const | Ruta a la carpeta. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Devuelve la prioridad de la fuente de fuentes. |
| [get_ScanSubfolders](./get_scansubfolders/)() const | Determina si escanear o no las subcarpetas. |
| [get_Type](./get_type/)() override | Devuelve el tipo de la fuente de fuentes. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Devuelve la lista de fuentes disponibles a través de esta fuente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo usar una carpeta del sistema local que contiene fuentes como una fuente de fuentes.
```cpp
// Crea una fuente de fuentes a partir de una carpeta que contiene archivos de fuentes.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Ver también

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
