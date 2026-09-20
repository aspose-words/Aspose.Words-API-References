---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Words 方法"
linktitle: "get_Words"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Words 方法。表示文档中单词数量的估计值（在 C++ 中）。"
type: docs
weight: 33000
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_words/
---
## BuiltInDocumentProperties::get_Words method


表示文档中单词数的估计值。

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Words()
```

## 备注


Aspose.Words 在调用 [UpdateWordCount](../../../aspose.words/document/updatewordcount/) 时更新此属性。

## 示例



展示如何在文档中更新所有列表标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words 不会实时跟踪此类文档指标。
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// 要获得这三个属性的准确值，我们需要手动更新它们。
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// 对于行数计数，我们需要调用更新方法的特定重载。
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## 另见

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
