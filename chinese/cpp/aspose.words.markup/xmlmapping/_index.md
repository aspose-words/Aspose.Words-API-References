---
title: "Aspose::Words::Markup::XmlMapping 类"
linktitle: "XmlMapping"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::XmlMapping 类。指定用于在父结构化文档标签和文档中存储于自定义 XML 数据部件内的 XML 元素之间建立映射的信息。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.markup/xmlmapping/
---
## XmlMapping class


指定用于在文档中建立父结构化文档标签与存储在自定义 XML 数据部件中的 XML 元素之间映射的信息。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。

```cpp
class XmlMapping : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Delete](./delete/)() | 删除父结构化文档与 XML 数据的映射。 |
| [get_CustomXmlPart](./get_customxmlpart/)() | 返回父结构化文档标签映射到的自定义 XML 数据部件。 |
| [get_IsMapped](./get_ismapped/)() | 如果父结构化文档标签成功映射到 XML 数据，则返回 **true**。 |
| [get_PrefixMappings](./get_prefixmappings/)() const | 返回用于评估 [XPath](./get_xpath/) 的 XML 命名空间前缀映射。 |
| [get_StoreItemId](./get_storeitemid/)() | 指定用于评估 [XPath](./get_xpath/) 表达式的自定义 XML 数据部件的标识符。 |
| [get_XPath](./get_xpath/)() const | 返回 XPath 表达式，该表达式用于查找映射到父结构化文档标签的自定义 XML 节点。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SetMapping](./setmapping/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&, const System::String\&, const System::String\&) | 设置父结构化文档标签与自定义 XML 数据部件的 XML 节点之间的映射。 |
| static [Type](./type/)() |  |

## 示例



展示如何为自定义 XML 部件设置 XML 映射。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 构建一个包含文本的 XML 部分并将其添加到文档的 CustomXmlPart 集合中。
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// 创建一个结构化文档标签，以显示我们 CustomXmlPart 的内容。
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);

// 为我们的结构化文档标签设置映射。此映射将指示
// 我们的结构化文档标签显示 XPath 指向的 XML 部分文本内容的一部分。
// 在这种情况下，它将是第一个 \"<root>\" 元素中第二个 \"<text>\" 元素的内容：\"Text element #2\"。
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", u"xmlns:ns='http://www.w3.org/2001/XMLSchema'");

ASSERT_TRUE(tag->get_XmlMapping()->get_IsMapped());
ASPOSE_ASSERT_EQ(xmlPart, tag->get_XmlMapping()->get_CustomXmlPart());
ASSERT_EQ(u"/root[1]/text[2]", tag->get_XmlMapping()->get_XPath());
ASSERT_EQ(u"xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag->get_XmlMapping()->get_PrefixMappings());

// 将结构化文档标签添加到文档，以显示我们自定义部分的内容。
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);
doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.XmlMapping.docx");
```

## 另见

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
