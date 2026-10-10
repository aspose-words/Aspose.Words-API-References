---
title: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance 方法"
linktitle: "get_DefaultInstance"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance 方法。C++ 中的静态默认字体设置。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


静态默认字体设置。

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## 示例



展示如何配置默认字体设置实例。
```cpp
// 配置默认字体设置实例以使用 "Courier New" 字体
// 作为在尝试使用未知字体时的备用替代。
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// 此文档没有 FontSettings 配置。渲染文档时，
// 默认的 FontSettings 实例将解析缺失的字体。
// Aspose.Words 将使用 "Courier New" 来渲染使用未知字体的文本。
ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontSettings()));

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontInstance.pdf");
```

## 另见

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
