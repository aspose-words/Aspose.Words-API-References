---
title: "Aspose::Words::Markup::CustomPart::Clone 方法"
linktitle: "克隆"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::CustomPart::Clone 方法。对对象进行“足够深度”的复制。在 C++ 中不复制 Data 值的字节。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.markup/custompart/clone/
---
## CustomPart::Clone method


创建对象的 "deep enough" 副本。不复制 [Data](../get_data/) 值的字节。

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomPart> Aspose::Words::Markup::CustomPart::Clone()
```


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
* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
