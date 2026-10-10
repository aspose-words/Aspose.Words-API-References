---
title: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource constructor"
linktitle: "FolderFontSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource constructor. Ctor en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource::FolderFontSource(const System::String\&, bool) constructor


Ctor.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| folderPath | const System::String\& | Ruta a la carpeta. |
| scanSubfolders | bool | Determina si escanear o no subcarpetas. |

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
## FolderFontSource::FolderFontSource(const System::String\&, bool, int32_t) constructor


Ctor.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders, int32_t priority)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| folderPath | const System::String\& | Ruta a la carpeta. |
| scanSubfolders | bool | Determina si escanear o no subcarpetas. |
| priority | int32_t | [Font](../../../aspose.words/font/) prioridad de origen. Consulte la descripción de la propiedad [Priority](../../fontsourcebase/get_priority/) para obtener más información. |

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
