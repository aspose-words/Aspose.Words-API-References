---
title: "Aspose::Words::Markup::CustomPart class"
linktitle: "CustomPart"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::CustomPart 类。表示一个自定义（任意内容）部件，该部件未在 ISO/IEC 29500 标准中定义。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.markup/custompart/
---
## CustomPart class


表示未被 ISO/IEC 29500 标准定义的自定义（任意内容）部件。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。

```cpp
class CustomPart : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clone](./clone/)() | 对对象进行 "deep enough" 复制。不会复制 [Data](./get_data/) 值的字节。 |
| [CustomPart](./custompart/)() |  |
| [get_ContentType](./get_contenttype/)() const | 指定此自定义部件的内容类型。 |
| [get_Data](./get_data/)() const | 包含此自定义部件的数据。 |
| [get_IsExternal](./get_isexternal/)() const | 如果此自定义部件存储在 OOXML 包内，则为 False；如果此自定义部件是外部目标，则为 True。 |
| [get_Name](./get_name/)() const | 获取或设置此部件在 OOXML 包内的绝对名称或目标 URL。 |
| [get_RelationshipType](./get_relationshiptype/)() const | 获取或设置从父部件到此自定义部件的关系类型。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContentType](./set_contenttype/)(const System::String\&) | 用于设置 [Aspose::Words::Markup::CustomPart::get_ContentType](./get_contenttype/) 的 setter。 |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | 用于设置 [Aspose::Words::Markup::CustomPart::get_Data](./get_data/) 的 setter。 |
| [set_IsExternal](./set_isexternal/)(bool) | 用于设置 [Aspose::Words::Markup::CustomPart::get_IsExternal](./get_isexternal/) 的 setter。 |
| [set_Name](./set_name/)(const System::String\&) | 用于设置 [Aspose::Words::Markup::CustomPart::get_Name](./get_name/) 的 setter。 |
| [set_RelationshipType](./set_relationshiptype/)(const System::String\&) | 用于设置 [Aspose::Words::Markup::CustomPart::get_RelationshipType](./get_relationshiptype/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


此类表示一个 OOXML 部件，它是“未知关系”的目标。所有未在 ISO/IEC 29500 中定义的关系均视为“未知关系”。只要符合关系标记指南，Office Open XML 文档中允许存在未知关系。

Microsoft Word 在打开/保存周期中保留自定义部件。可以在此处找到更多信息 [http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx](http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx)

Aspose.Words 也会在往返过程中保留自定义部件，此外，还允许通过 [CustomPart](./) 和 [CustomPartCollection](../custompartcollection/) 对象以编程方式访问这些部件。

不要将自定义部件与自定义 XML 数据混淆。如果需要访问自定义 XML 数据，请使用 [CustomXmlPart](../customxmlpart/)。

## 示例



展示如何访问文档的任意自定义部件集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// 克隆第二个部件，然后将克隆添加到集合中。
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// 遍历集合并打印每个部件。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// 我们可以单独或一次性地从此集合中移除元素。
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## 另见

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
