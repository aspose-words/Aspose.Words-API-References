---
title: "Aspose::Words::Document::get_HyphenationOptions 方法"
linktitle: "get_HyphenationOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_HyphenationOptions 方法。提供对 C++ 中文档连字符选项的访问。"
type: docs
weight: 32000
url: /zh/cpp/aspose.words/document/get_hyphenationoptions/
---
## Document::get_HyphenationOptions method


提供对文档连字符选项的访问。

```cpp
System::SharedPtr<Aspose::Words::Settings::HyphenationOptions> Aspose::Words::Document::get_HyphenationOptions()
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

* Class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
