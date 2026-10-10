---
title: "Aspose::Words::Fonts::FolderFontSource::get_FolderPath método"
linktitle: "get_FolderPath"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FolderFontSource::get_FolderPath método. Ruta a la carpeta en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fonts/folderfontsource/get_folderpath/
---
## FolderFontSource::get_FolderPath method


Ruta a la carpeta.

```cpp
System::String Aspose::Words::Fonts::FolderFontSource::get_FolderPath() const
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

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
