---
title: "Aspose::Words::Markup::XmlMapping::get_StoreItemId method"
linktitle: "get_StoreItemId"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::XmlMapping::get_StoreItemId 方法。指定用于在 C++ 中评估 XPath 表达式的自定义 XML 数据部件的标识符。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.markup/xmlmapping/get_storeitemid/
---
## XmlMapping::get_StoreItemId method


指定用于评估 [XPath](../get_xpath/) 表达式的自定义 XML 数据部件的标识符。

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_StoreItemId()
```


## 示例



展示如何获取 XML 部件的自定义 XML 数据标识符。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom XML part in structured document tag.docx");

// 结构化文档标签的 ID 采用 GUID 形式。
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 0, true));

ASSERT_EQ(u"{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag->get_XmlMapping()->get_StoreItemId());
```

## 另见

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
