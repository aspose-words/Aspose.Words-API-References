---
title: "Aspose::Words::Node::get_Range 方法"
linktitle: "get_Range"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Node::get_Range 方法。返回一个 Range 对象，表示此节点中包含的文档部分，在 C++ 中。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/node/get_range/
---
## Node::get_Range method


返回一个 [Range](../../range/) 对象，表示此节点中包含的文档部分。

```cpp
System::SharedPtr<Aspose::Words::Range> Aspose::Words::Node::get_Range()
```


## 示例



展示如何从范围中删除所有节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 向文档的第一个节添加文本，然后再添加另一个节。
builder->Write(u"Section 1. ");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Write(u"Section 2.");

ASSERT_EQ(u"Section 1. \fSection 2.", doc->GetText().Trim());

// 通过删除所有节点，完全移除第一节
// 在其范围内，包括该节本身。
doc->get_Sections()->idx_get(0)->get_Range()->Delete();

ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(u"Section 2.", doc->GetText().Trim());
```

## 另见

* Class [Range](../../range/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
