---
title: "Aspose::Words::Fonts::FolderFontSource::get_FolderPath 方法"
linktitle: "get_FolderPath"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FolderFontSource::get_FolderPath 方法。C++ 中的文件夹路径。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fonts/folderfontsource/get_folderpath/
---
## FolderFontSource::get_FolderPath method


文件夹的路径。

```cpp
System::String Aspose::Words::Fonts::FolderFontSource::get_FolderPath() const
```


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

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
