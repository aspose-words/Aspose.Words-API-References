---
title: "Aspose::Words::Fonts::FileFontSource::get_FilePath 方法"
linktitle: "get_FilePath"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FileFontSource::get_FilePath 方法。字体文件的路径（C++）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.fonts/filefontsource/get_filepath/
---
## FileFontSource::get_FilePath method


字体文件的路径。

```cpp
System::String Aspose::Words::Fonts::FileFontSource::get_FilePath() const
```


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

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
