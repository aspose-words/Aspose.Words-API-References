---
title: "Aspose::Words::Fonts::FontSourceBase::get_Priority 方法"
linktitle: "get_Priority"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontSourceBase::get_Priority 方法。返回 C++ 中字体源的优先级。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fonts/fontsourcebase/get_priority/
---
## FontSourceBase::get_Priority method


返回字体源的优先级。

```cpp
int32_t Aspose::Words::Fonts::FontSourceBase::get_Priority() const
```

## 备注


当不同字体源中存在具有相同族名和样式的字体时，会使用此值。在这种情况下，Aspose.Words 会从优先级更高的源中选择字体。

默认值为 0。

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

* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
