---
title: "Aspose::Words::Range::Delete method"
linktitle: "删除"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Range::Delete method. 删除范围内的所有字符（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/range/delete/
---
## Range::Delete method


删除范围内的所有字符。

```cpp
void Aspose::Words::Range::Delete()
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

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
