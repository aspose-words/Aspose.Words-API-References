---
title: "Aspose::Words::Section::ClearContent method"
linktitle: "ClearContent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Section::ClearContent 方法。清除 C++ 中的节。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/section/clearcontent/
---
## Section::ClearContent method


清除该节。

```cpp
void Aspose::Words::Section::ClearContent()
```

## 备注


[Body](../get_body/) 的文本被清除，只剩下一个空段落，表示节分隔符。

所有页眉和页脚的文本被清除，但 [HeaderFooter](../../headerfooter/) 对象本身未被删除。

## 示例



展示如何清除节的内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// 运行 "ClearContent" 方法将删除所有节内容
// 但会留下一个空段落，以便再次添加内容。
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## 另见

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
