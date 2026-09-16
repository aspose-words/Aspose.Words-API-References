---
title: "Aspose::Words::Fonts::FolderFontSource 类"
linktitle: "FolderFontSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FolderFontSource 类。表示包含 TrueType 字体文件的文件夹。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


表示包含 TrueType 字体文件的文件夹。要了解更多信息，请访问 [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) 文档文章。

```cpp
class FolderFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool) | 构造函数。 |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool, int32_t) | 构造函数。 |
| [get_FolderPath](./get_folderpath/)() const | 文件夹的路径。 |
| [get_Priority](../fontsourcebase/get_priority/)() const | 返回字体源的优先级。 |
| [get_ScanSubfolders](./get_scansubfolders/)() const | 确定是否扫描子文件夹。 |
| [get_Type](./get_type/)() override | 返回字体源的类型。 |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | 在处理字体源时调用，如果检测到可能导致格式保真度损失的问题。 |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 在处理字体源时调用，如果检测到可能导致格式保真度损失的问题。 |
| static [Type](./type/)() |  |

## 示例



展示如何使用包含字体的本地系统文件夹作为字体源。
```cpp
// 从包含字体文件的文件夹创建字体源。
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## 另见

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
