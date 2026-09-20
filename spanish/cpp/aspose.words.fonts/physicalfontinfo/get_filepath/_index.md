---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath método"
linktitle: "get_FilePath"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath método. Ruta al archivo de fuente si existe en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fonts/physicalfontinfo/get_filepath/
---
## PhysicalFontInfo::get_FilePath method


Ruta al archivo de fuente, si existe.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath() const
```


## Ejemplos



Muestra cómo enumerar las fuentes disponibles.
```cpp
// Configure Aspose.Words para obtener fuentes de una carpeta personalizada y luego imprima cada fuente disponible.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## Ver también

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
