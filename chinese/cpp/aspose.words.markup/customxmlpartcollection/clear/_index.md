---
title: "Aspose::Words::Markup::CustomXmlPartCollection::Clear method"
linktitle: "清除"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::CustomXmlPartCollection::Clear 方法。删除集合中的所有元素（在 C++ 中）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.markup/customxmlpartcollection/clear/
---
## CustomXmlPartCollection::Clear method


从集合中移除所有元素。

```cpp
void Aspose::Words::Markup::CustomXmlPartCollection::Clear()
```


## 示例



展示如何使用自定义 XML 数据创建结构化文档标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 构建一个包含数据的 XML 部件并将其添加到文档的集合中。
// 如果我们在 Microsoft Word 中启用 "Developer" 选项卡，
// 我们可以在 "XML Mapping Pane" 中找到此集合的元素，以及一些默认元素。
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// 下面有两种引用 XML 部件的方式。
// 1 -  通过自定义 XML 部件集合中的索引：
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  通过 GUID：
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// 添加 XML 架构关联。
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// 克隆一个部件，然后将其插入集合中。
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// 遍历集合并打印每个部件的内容。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"XML part index {0}, ID: {1}", index, enumerator->get_Current()->get_Id()) << std::endl;
        std::cout << System::String::Format(u"\tContent: {0}", System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data())) << std::endl;
        index++;
    }
}

// 使用 "RemoveAt" 方法通过索引删除克隆的部件。
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// 克隆 XML 部件集合，然后使用 "Clear" 方法一次性删除其所有元素。
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// 创建一个结构化文档标签，以显示我们部件的内容并将其插入文档主体。
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## 另见

* Class [CustomXmlPartCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
