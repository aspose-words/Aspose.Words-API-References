---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_Version método"
linktitle: "get_Version"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_Version método. Cadena de versión de la fuente en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.fonts/physicalfontinfo/get_version/
---
## PhysicalFontInfo::get_Version method


Cadena de versión de la fuente.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_Version() const
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
