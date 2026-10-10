---
title: "Aspose::Words::Fonts::PhysicalFontInfo 类"
linktitle: "PhysicalFontInfo"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::PhysicalFontInfo 类。指定可供 Aspose.Words 字体引擎使用的物理字体信息。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class


指定 Aspose.Words 字体引擎可用的物理字体信息。欲了解更多，请访问[Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/)文档文章。

```cpp
class PhysicalFontInfo : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() const | 嵌入字体的许可权。 |
| [get_FilePath](./get_filepath/)() const | 字体文件的路径（如果有）。 |
| [get_FontFamilyName](./get_fontfamilyname/)() const | 字体的族名称。 |
| [get_FullFontName](./get_fullfontname/)() const | 字体的完整名称。 |
| [get_Version](./get_version/)() const | 字体的版本字符串。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
