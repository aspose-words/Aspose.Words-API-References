---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_FullFontName метод"
linktitle: "get_FullFontName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_FullFontName метод. Полное название шрифта в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fonts/physicalfontinfo/get_fullfontname/
---
## PhysicalFontInfo::get_FullFontName method


Полное имя шрифта.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FullFontName() const
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

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
