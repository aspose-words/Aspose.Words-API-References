---
title: "Aspose::Words::Fonts::FontSourceType 枚举"
linktitle: "FontSourceType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontSourceType 枚举。指定 C++ 中字体源的类型。"
type: docs
weight: 23000
url: /zh/cpp/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enum


指定字体源的类型。

```cpp
enum class FontSourceType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| FontFile | 0 | 一个表示单个字体文件的 [FileFontSource](../filefontsource/) 对象。 |
| FontsFolder | 1 | 一个表示包含字体文件的文件夹的 [FolderFontSource](../folderfontsource/) 对象。 |
| MemoryFont | 2 | 一个表示内存中单个字体的 [MemoryFontSource](../memoryfontsource/) 对象。 |
| SystemFonts | 3 | 一个表示系统中已安装的所有字体的 [SystemFontSource](../systemfontsource/) 对象。 |
| FontStream | 4 | 一个表示包含字体数据流的 [StreamFontSource](../streamfontsource/) 对象。 |


## 示例



展示如何在本地文件系统中将字体文件用作字体来源。
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## 另见

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
