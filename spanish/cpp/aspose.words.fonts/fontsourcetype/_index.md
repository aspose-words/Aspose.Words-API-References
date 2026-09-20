---
title: "Aspose::Words::Fonts::FontSourceType enumeración"
linktitle: "FontSourceType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontSourceType enum. Especifica el tipo de origen de fuente en C++."
type: docs
weight: 23000
url: /es/cpp/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enum


Especifica el tipo de fuente de origen.

```cpp
enum class FontSourceType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| FontFile | 0 | Un objeto [FileFontSource](../filefontsource/) que representa un archivo de fuente único. |
| FontsFolder | 1 | Un objeto [FolderFontSource](../folderfontsource/) que representa una carpeta con archivos de fuentes. |
| MemoryFont | 2 | Un objeto [MemoryFontSource](../memoryfontsource/) que representa una fuente única en memoria. |
| SystemFonts | 3 | Un objeto [SystemFontSource](../systemfontsource/) que representa todas las fuentes instaladas en el sistema. |
| FontStream | 4 | Un objeto [StreamFontSource](../streamfontsource/) que representa una secuencia con datos de fuentes. |


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
