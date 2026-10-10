---
title: "Aspose::Words::Markup::CustomPartCollection::Add 方法"
linktitle: "Add"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::CustomPartCollection::Add 方法。向集合中添加项（在 C++ 中）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.markup/custompartcollection/add/
---
## CustomPartCollection::Add method


向集合中添加一个项。

```cpp
void Aspose::Words::Markup::CustomPartCollection::Add(const System::SharedPtr<Aspose::Words::Markup::CustomPart> &part)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 部件 | const System::SharedPtr\<Aspose::Words::Markup::CustomPart\>\& | 要添加的项。 |

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

* Class [CustomPart](../../custompart/)
* Class [CustomPartCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
