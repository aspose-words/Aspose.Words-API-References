---
title: "Aspose::Words::DocumentBase::get_Document 方法"
linktitle: "get_Document"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBase::get_Document 方法。获取此实例（在 C++ 中）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/documentbase/get_document/
---
## DocumentBase::get_Document method


获取此实例。

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::DocumentBase::get_Document() const override
```


## 示例



展示如何创建简单文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 新的 Document 对象默认带有最小节点集
// 需要开始添加内容（如文本和形状）：一个 Section、一个 Body 和一个 Paragraph。
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## 另见

* Class [DocumentBase](../)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
