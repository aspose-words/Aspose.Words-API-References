---
title: "Aspose::Words::Document::get_Compliance 方法"
linktitle: "get_Compliance"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_Compliance 方法。获取从已加载文档内容确定的 OOXML 合规版本。仅在 C++ 中的 OOXML 文档中有意义。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words/document/get_compliance/
---
## Document::get_Compliance method


获取从加载的文档内容确定的 OOXML 合规版本。仅对 OOXML 文档有意义。

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```

## 备注


如果您创建了一个新的空白文档或加载非 OOXML 文档，则返回 [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/) 值。

## 示例



展示如何读取已加载文档的 Open Office XML 合规版本。
```cpp
// 合规版本在不同版本的 Microsoft Word 创建的文档之间会有所不同。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.doc");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Ecma376_2006);

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);
```

## 另见

* Enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
