---
title: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get 方法。根据索引返回 DocumentProperty 对象（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.properties/documentpropertycollection/idx_get/
---
## DocumentPropertyCollection::idx_get(int32_t) method


根据索引返回一个 [DocumentProperty](../../documentproperty/) 对象。

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 要检索的 [DocumentProperty](../../documentproperty/) 的零基索引。 |

## 示例



展示如何使用自定义文档属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// 每个文档都包含一组自定义属性，这些属性与内置属性一样，都是键值对。
// 文档具有固定的内置属性列表。用户创建所有自定义属性。
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```

## 另见

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentPropertyCollection::idx_get(System::String) method


根据属性名称返回一个 [DocumentProperty](../../documentproperty/) 对象。

```cpp
virtual System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(System::String name)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | System::String | 要检索的属性名称（不区分大小写）。 |
## 备注


如果未找到具有指定名称的属性，则返回 **null**。

## 示例



展示如何创建包含日期和时间的自定义文档属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```

## 另见

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
