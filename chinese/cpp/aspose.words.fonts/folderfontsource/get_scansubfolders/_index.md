---
title: "Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders 方法"
linktitle: "get_ScanSubfolders"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders 方法。确定是否在 C++ 中扫描子文件夹。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.fonts/folderfontsource/get_scansubfolders/
---
## FolderFontSource::get_ScanSubfolders method


确定是否扫描子文件夹。

```cpp
bool Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders() const
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
