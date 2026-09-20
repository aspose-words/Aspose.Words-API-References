---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping 方法"
linktitle: "get_XmlMapping"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping 方法。获取一个对象，表示此结构化文档标签范围在当前文档的自定义 XML 部分中的 XML 数据映射（C++）。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words.markup/structureddocumenttagrangestart/get_xmlmapping/
---
## StructuredDocumentTagRangeStart::get_XmlMapping method


获取一个对象，表示此结构化文档标签范围到当前文档自定义 XML 部分中 XML 数据的映射。

```cpp
System::SharedPtr<Aspose::Words::Markup::XmlMapping> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping() override
```


## 示例



展示如何为结构化文档标签的范围起始设置 XML 映射。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

// 构建一个包含文本的 XML 部分并将其添加到文档的 CustomXmlPart 集合中。
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// 创建一个结构化文档标签，使其在文档中显示我们 CustomXmlPart 的内容。
auto sdtRangeStart = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

// 如果我们为结构化文档标签设置映射，
// 它只会显示 XPath 所指向的 CustomXmlPart 的一部分。
// 此 XPath 将指向我们 CustomXmlPart 中第一个 \"<root>\" 元素的第二个 \"<text>\" 元素的内容。
sdtRangeStart->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", nullptr);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

## 另见

* Class [XmlMapping](../../xmlmapping/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
