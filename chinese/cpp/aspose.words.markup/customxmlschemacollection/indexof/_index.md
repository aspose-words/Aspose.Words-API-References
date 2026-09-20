---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection::IndexOf 方法"
linktitle: "IndexOf"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection::IndexOf 方法。在 C++ 中返回集合中指定值的零基索引。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.markup/customxmlschemacollection/indexof/
---
## CustomXmlSchemaCollection::IndexOf method


返回集合中指定值的零基索引。

```cpp
int32_t Aspose::Words::Markup::CustomXmlSchemaCollection::IndexOf(const System::String &value)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | const System::String\& | 要定位的区分大小写的值。 |

### ReturnValue

零基索引。如果未找到则为负值。

## 示例



展示如何使用 XML 架构集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// 添加 XML 架构关联。
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// 克隆自定义 XML 部分的 XML 架构关联集合，
// 然后向克隆中添加几个新架构。
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// 枚举这些架构并打印每个元素。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// 下面是从集合中移除架构的三种方法。
// 1 -  按索引移除架构：
schemas->RemoveAt(2);

// 2 -  按值移除架构：
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  使用 \"Clear\" 方法一次性清空集合。
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## 另见

* Class [CustomXmlSchemaCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
