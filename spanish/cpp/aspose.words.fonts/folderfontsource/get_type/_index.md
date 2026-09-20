---
title: "Aspose::Words::Fonts::FolderFontSource::get_Type método"
linktitle: "get_Type"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FolderFontSource::get_Type método. Devuelve el tipo del origen de la fuente en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.fonts/folderfontsource/get_type/
---
## FolderFontSource::get_Type method


Devuelve el tipo de la fuente de fuentes.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FolderFontSource::get_Type() override
```


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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
