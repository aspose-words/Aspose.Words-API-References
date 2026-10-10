---
title: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource 构造函数"
linktitle: "FolderFontSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource 构造函数。C++ 中的构造函数。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource::FolderFontSource(const System::String\&, bool) constructor


构造函数。

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| folderPath | const System::String\& | 文件夹路径。 |
| scanSubfolders | bool | 确定是否扫描子文件夹。 |

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
## FolderFontSource::FolderFontSource(const System::String\&, bool, int32_t) constructor


构造函数。

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders, int32_t priority)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| folderPath | const System::String\& | 文件夹路径。 |
| scanSubfolders | bool | 确定是否扫描子文件夹。 |
| priority | int32_t | [Font](../../../aspose.words/font/) 源优先级。有关更多信息，请参阅 [Priority](../../fontsourcebase/get_priority/) 属性描述。 |

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
