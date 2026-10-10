---
title: "Aspose::Words::Markup::CustomPart::get_ContentType 方法"
linktitle: "get_ContentType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::CustomPart::get_ContentType 方法。指定此自定义部件在 C++ 中的内容类型。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.markup/custompart/get_contenttype/
---
## CustomPart::get_ContentType method


指定此自定义部件的内容类型。

```cpp
System::String Aspose::Words::Markup::CustomPart::get_ContentType() const
```

## 备注


仅当 [IsExternal](../get_isexternal/) 为 **false** 时，此属性适用。

默认值为空字符串。有效值必须为非空字符串。

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

* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
