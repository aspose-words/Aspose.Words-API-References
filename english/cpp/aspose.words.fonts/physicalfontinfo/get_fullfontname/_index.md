---
title: get_FullFontName
second_title: Aspose.Words for C++ API Reference
description: Full name of the font.
type: docs
weight: 27
url: /cpp/aspose.words.fonts/physicalfontinfo/get_fullfontname/
---
## PhysicalFontInfo.get_FullFontName method


Full name of the font.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FullFontName() const
```


## Examples




Shows how to list available fonts. 
```cpp
// Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
ArrayPtr<SharedPtr<FontSourceBase>> folderFontSource = MakeArray<SharedPtr<FontSourceBase>>({MakeObject<FolderFontSource>(FontsDir, true)});

for (const auto& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

