---
title: "Aspose::Words::Fonts::FileFontSource::get_Type 方法"
linktitle: "get_Type"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FileFontSource::get_Type 方法。返回 C++ 中字体来源的类型。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.fonts/filefontsource/get_type/
---
## FileFontSource::get_Type method


返回字体源的类型。

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FileFontSource::get_Type() override
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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
