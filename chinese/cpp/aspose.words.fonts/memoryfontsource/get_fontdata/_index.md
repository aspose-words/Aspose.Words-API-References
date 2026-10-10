---
title: "Aspose::Words::Fonts::MemoryFontSource::get_FontData 方法"
linktitle: "get_FontData"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::MemoryFontSource::get_FontData 方法。C++ 中的二进制字体数据。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.fonts/memoryfontsource/get_fontdata/
---
## MemoryFontSource::get_FontData method


二进制字体数据。

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::MemoryFontSource::get_FontData() const
```


## 示例



展示如何使用包含字体文件数据的字节数组作为字体源。
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## 另见

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
