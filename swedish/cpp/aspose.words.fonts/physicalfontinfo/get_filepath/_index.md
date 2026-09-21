---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath method"
linktitle: "get_FilePath"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath‑metoden. Sökväg till teckensnittsfilen, om någon, i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fonts/physicalfontinfo/get_filepath/
---
## PhysicalFontInfo::get_FilePath method


Sökväg till teckensnittsfilen, om någon.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath() const
```


## Exempel



Visar hur man listar tillgängliga teckensnitt.
```cpp
// Konfigurera Aspose.Words för att hämta teckensnitt från en anpassad mapp, och skriv sedan ut varje tillgängligt teckensnitt.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## Se även

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
