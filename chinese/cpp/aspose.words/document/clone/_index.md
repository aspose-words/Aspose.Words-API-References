---
title: "Aspose::Words::Document::Clone 方法"
linktitle: "克隆"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::Clone 方法。在 C++ 中对 Document 执行深度复制。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/document/clone/
---
## Document::Clone method


对 [Document](../) 执行深度复制。

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::Clone()
```


### ReturnValue

克隆的文档。

## 示例



展示如何对文档进行深度克隆。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

// 克隆将生成一个与原始文档内容相同的新文档，
// 但每个原始文档的节点都有唯一的副本。
System::SharedPtr<Aspose::Words::Document> clone = doc->Clone();

ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->GetText(), clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_NE(System::ObjectExt::GetHashCode(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)), System::ObjectExt::GetHashCode(clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)));
```

## 另见

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
