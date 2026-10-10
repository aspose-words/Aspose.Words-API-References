---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath 方法"
linktitle: "get_FilePath"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath 方法。C++ 中字体文件的路径（如果有）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fonts/physicalfontinfo/get_filepath/
---
## PhysicalFontInfo::get_FilePath method


字体文件的路径（如果有）。

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath() const
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

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
