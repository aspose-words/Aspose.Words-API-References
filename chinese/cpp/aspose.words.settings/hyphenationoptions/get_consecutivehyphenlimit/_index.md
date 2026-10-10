---
title: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit 方法"
linktitle: "get_ConsecutiveHyphenLimit"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit 方法。获取或设置可以以连字符结尾的连续行的最大数量。此属性在 C++ 中的默认值为 0。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.settings/hyphenationoptions/get_consecutivehyphenlimit/
---
## HyphenationOptions::get_ConsecutiveHyphenLimit method


获取或设置可以以连字符结尾的连续行的最大数量。此属性的默认值为 0。

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit() const
```

## 备注


如果此属性的值设置为 0，则任意数量的连续行都可以以连字符结尾。

在保存为固定页面格式（例如 PDF）时，此属性不产生作用。

## 示例



展示如何配置自动连字。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## 另见

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
