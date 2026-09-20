---
title: "Aspose::Words::Fonts::StreamFontSource class"
linktitle: "StreamFontSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::StreamFontSource class. 用户自定义流字体来源的基类。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class


用户自定义流字体源的基类。欲了解更多，请访问[Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/)文档文章。

```cpp
class StreamFontSource : public Aspose::Words::Fonts::FontSourceBase,
                         public Aspose::Fonts::IFontData
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | 此来源在缓存中的键。 |
| [get_IsEmbedded](./get_isembedded/)() override |  |
| [get_Priority](../fontsourcebase/get_priority/)() const | 返回字体源的优先级。 |
| [get_Type](./get_type/)() override | 返回字体源的类型。 |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | 在处理字体源时调用，如果检测到可能导致格式保真度损失的问题。 |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [OpenFontDataStream](./openfontdatastream/)() | 此方法应按需打开包含字体数据的流。 |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 在处理字体源时调用，如果检测到可能导致格式保真度损失的问题。 |
| static [Type](./type/)() |  |
## 备注


为了使用流字体源，您应该从 [StreamFontSource](./) 派生一个类，并提供对 [OpenFontDataStream](./openfontdatastream/) 方法的实现。

[OpenFontDataStream](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime. 
## 另见

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
