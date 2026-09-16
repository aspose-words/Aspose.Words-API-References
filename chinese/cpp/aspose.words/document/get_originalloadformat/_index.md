---
title: "Aspose::Words::Document::get_OriginalLoadFormat 方法"
linktitle: "get_OriginalLoadFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_OriginalLoadFormat 方法。获取加载到此对象中的原始文档的格式（C++）。"
type: docs
weight: 41000
url: /zh/cpp/aspose.words/document/get_originalloadformat/
---
## Document::get_OriginalLoadFormat method


获取加载到此对象中的原始文档的格式。

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```

## 备注


如果您创建了一个新的空白文档，则返回 [Doc](../../loadformat/) 值。

## 示例



展示如何检索文档加载操作的详细信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

## 另见

* Enum [LoadFormat](../../loadformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
