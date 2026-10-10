---
title: "Aspose::Words::Document::UpdateWordCount 方法"
linktitle: "UpdateWordCount"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::UpdateWordCount 方法。更新文档在 C++ 中的字数统计属性。"
type: docs
weight: 101000
url: /zh/cpp/aspose.words/document/updatewordcount/
---
## Document::UpdateWordCount() method


更新文档的字数统计属性。

```cpp
void Aspose::Words::Document::UpdateWordCount()
```

## 备注


[UpdateWordCount](./) recalculates and updates Characters, [Words](../../) and Paragraphs properties in the [BuiltInDocumentProperties](../get_builtindocumentproperties/) collection of the [Document](../).

请注意，[UpdateWordCount](./) 不会更新行数和页数属性。使用 [UpdateWordCount](./) 重载并传递 **true** 值作为参数即可实现此目的。

当您使用评估版时，评估水印也会计入字数统计。

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateWordCount(bool) method


更新文档的字数统计属性，可选地更新 [Lines](../../../aspose.words.properties/builtindocumentproperties/get_lines/) 属性。

```cpp
void Aspose::Words::Document::UpdateWordCount(bool updateLinesCount)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| updateLinesCount | bool | **true** 如果应计算文档中的行数。 |

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
