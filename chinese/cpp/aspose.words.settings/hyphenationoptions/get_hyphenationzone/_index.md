---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone 方法"
linktitle: "get_HyphenationZone"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone 方法。获取或设置从右边距起的距离（以 1/20 点为单位），在此范围内不进行单词连字。此属性的默认值在 C++ 中为 360（0.25 英寸）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.settings/hyphenationoptions/get_hyphenationzone/
---
## HyphenationOptions::get_HyphenationZone method


获取或设置从右边距起的距离（以 1/20 点为单位），在此范围内不进行连字。此属性的默认值为 360（0.25 英寸）。

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone() const
```


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
