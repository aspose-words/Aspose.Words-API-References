---
title: "Aspose::Words::Font::get_NameFarEast method"
linktitle: "get_NameFarEast"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_NameFarEast 方法。返回或设置 C++ 中的东亚字体名称。"
type: docs
weight: 28000
url: /zh/cpp/aspose.words/font/get_namefareast/
---
## Font::get_NameFarEast method


返回或设置东亚字体名称。

```cpp
System::String Aspose::Words::Font::get_NameFarEast()
```


## 示例



展示如何在东亚语言中插入和格式化文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 指定文档生成器将应用于其插入的任何文本的字体设置。
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// 为我们的字体和区域命名 “FarEast” 等价项。
// 如果生成器使用此字体配置插入亚洲字符，则每个包含这些字符的运行
// 这些字符将使用 “FarEast” 字体/区域而不是默认设置进行显示。
// 当西文字体无法对亚洲字符提供理想的表现时，这可能会很有用。
builder->get_Font()->set_NameFarEast(u"SimSun");
builder->get_Font()->set_LocaleIdFarEast(System::MakeObject<System::Globalization::CultureInfo>(u"zh-CN", false)->get_LCID());

// 此文本将以默认的字体/区域显示。
builder->Writeln(u"Hello world!");

// 由于这些是亚洲字符，此运行将应用我们的 “FarEast” 字体/区域等价项。
builder->Writeln(u"你好世界");

doc->Save(get_ArtifactsDir() + u"Font.FarEast.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
