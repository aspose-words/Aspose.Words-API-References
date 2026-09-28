---
title: "Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts метод"
linktitle: "GetAvailableFonts"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts метод. Возвращает список шрифтов, доступных через этот источник, в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase::GetAvailableFonts method


Возвращает список шрифтов, доступных через этот источник.

```cpp
System::SharedPtr<System::Collections::Generic::IList<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>>> Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts()
```


## Примеры



Показывает, как перечислить доступные шрифты.
```cpp
// Настройте Aspose.Words для получения шрифтов из пользовательской папки, а затем выведите каждый доступный шрифт.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## См. также

* Class [PhysicalFontInfo](../../physicalfontinfo/)
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
