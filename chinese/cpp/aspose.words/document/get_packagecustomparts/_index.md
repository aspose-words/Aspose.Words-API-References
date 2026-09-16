---
title: "Aspose::Words::Document::get_PackageCustomParts 方法"
linktitle: "get_PackageCustomParts"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_PackageCustomParts 方法。获取或设置与 OOXML 包使用“未知关系”链接的自定义部件（任意内容）集合（C++）。"
type: docs
weight: 42000
url: /zh/cpp/aspose.words/document/get_packagecustomparts/
---
## Document::get_PackageCustomParts method


获取或设置使用 "unknown relationships" 链接到 OOXML 包的自定义部件（任意内容）集合。

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomPartCollection> Aspose::Words::Document::get_PackageCustomParts() const
```

## 备注


不要将这些自定义部件与 Custom XML 数据混淆。如果需要访问 Custom XML 部件，请使用 [CustomXmlParts](../get_customxmlparts/) 属性。

此集合包含父级为 OOXML 包且目标为“未知关系”的 OOXML 部件。更多信息请参见 [CustomPart](../../../aspose.words.markup/custompart/)。

Aspose.Words 仅将自定义部件加载并保存到 OOXML 文档中。

此属性不能为 **null**。

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

* Class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
