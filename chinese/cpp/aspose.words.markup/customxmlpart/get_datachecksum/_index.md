---
title: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum 方法"
linktitle: "get_DataChecksum"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum 方法。指定在 C++ 中 Data 内容的循环冗余校验（CRC）校验和。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.markup/customxmlpart/get_datachecksum/
---
## CustomXmlPart::get_DataChecksum method


指定 [Data](../get_data/) 内容的循环冗余校验（CRC）校验和。

```cpp
int64_t Aspose::Words::Markup::CustomXmlPart::get_DataChecksum()
```


## 示例



展示在运行时如何计算校验和。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto richText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(richText);

// 校验和是只读的，并使用相应自定义 XML 数据部件的数据进行计算。
richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>ContentControl</text></root>"), u"/root/text", u"");

int64_t checksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << checksum << std::endl;

richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>Updated ContentControl</text></root>"), u"/root/text", u"");

int64_t updatedChecksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << updatedChecksum << std::endl;

// 我们更改了标签的 XmlPart，校验和在运行时已更新。
ASSERT_NE(checksum, updatedChecksum);
```

## 另见

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
