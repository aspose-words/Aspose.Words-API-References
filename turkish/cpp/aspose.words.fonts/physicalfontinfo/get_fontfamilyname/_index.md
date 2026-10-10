---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_FontFamilyName yöntemi"
linktitle: "get_FontFamilyName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_FontFamilyName yöntemi. C++'ta fontun aile adı."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fonts/physicalfontinfo/get_fontfamilyname/
---
## PhysicalFontInfo::get_FontFamilyName method


Yazı tipinin aile adı.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FontFamilyName() const
```


## Örnekler



Kullanılabilir yazı tiplerini listeleme yöntemini gösterir.
```cpp
// Aspose.Words'ü özel bir klasörden yazı tipleri alacak şekilde yapılandırın ve ardından her kullanılabilir yazı tipini yazdırın.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## Ayrıca Bakınız

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
