---
title: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens 方法"
linktitle: "get_SuppressAutoHyphens"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens 方法。指定当前段落是否应免除文档设置中应用的任何连字（在 C++ 中）。"
type: docs
weight: 38000
url: /zh/cpp/aspose.words/paragraphformat/get_suppressautohyphens/
---
## ParagraphFormat::get_SuppressAutoHyphens method


指定当前段落是否应免除文档设置中应用的任何连字符处理。

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens()
```


## 示例



展示如何为段落抑制连字。
```cpp
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// 打开一个包含文本的文档，其语言环境与我们的词典匹配。
// 当我们将此文档保存为固定页面格式时，其文本将会出现连字。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

// 我们可以将 "SuppressAutoHyphens" 属性设置为 "true" 来禁用连字
// 针对特定段落，同时保持文档其余部分的连字功能开启。
// 此属性的默认值为 "false"，
// 这意味着默认情况下，每个段落如果有可用的连字则会使用。
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.SuppressHyphens.pdf");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
