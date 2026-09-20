---
title: "Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts 方法"
linktitle: "GetAvailableFonts"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts 方法。返回 C++ 中此源可用的字体列表。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase::GetAvailableFonts method


返回通过此源可用的字体列表。

```cpp
System::SharedPtr<System::Collections::Generic::IList<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>>> Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts()
```


## 示例



展示如何列出可用字体。
```cpp
// 配置 Aspose.Words 从自定义文件夹获取字体，然后打印所有可用字体。
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## 另见

* Class [PhysicalFontInfo](../../physicalfontinfo/)
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
