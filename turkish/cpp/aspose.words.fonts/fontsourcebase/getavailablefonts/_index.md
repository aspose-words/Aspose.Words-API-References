---
title: "Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts metodu"
linktitle: "GetAvailableFonts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts metodu. Bu kaynak üzerinden kullanılabilir fontların listesini C++'da döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase::GetAvailableFonts method


Bu kaynak üzerinden kullanılabilir yazı tiplerinin listesini döndürür.

```cpp
System::SharedPtr<System::Collections::Generic::IList<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>>> Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts()
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

* Class [PhysicalFontInfo](../../physicalfontinfo/)
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
