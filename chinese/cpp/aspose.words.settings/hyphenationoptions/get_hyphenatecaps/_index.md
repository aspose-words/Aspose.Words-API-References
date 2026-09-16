---
title: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps 方法"
linktitle: "get_HyphenateCaps"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps 方法。获取或设置决定是否对全大写单词进行连字的值。此属性在 C++ 中的默认值为 true。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.settings/hyphenationoptions/get_hyphenatecaps/
---
## HyphenationOptions::get_HyphenateCaps method


获取或设置决定全大写单词是否进行连字的值。此属性的默认值为 **true**。

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps() const
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
