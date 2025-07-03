---
title: Aspose::Words::Fonts::PhysicalFontInfo::get_FullFontName method
linktitle: get_FullFontName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::PhysicalFontInfo::get_FullFontName method. Full name of the font in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fonts/physicalfontinfo/get_fullfontname/
---
## PhysicalFontInfo::get_FullFontName method


Full name of the font.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FullFontName() const
```


## Examples



Shows how to list available fonts. 
```cpp
// Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## See Also

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
