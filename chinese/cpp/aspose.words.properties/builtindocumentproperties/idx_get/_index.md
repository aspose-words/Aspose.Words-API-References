---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get 方法。 在 C++ 中，根据属性名称返回一个 DocumentProperty 对象。"
type: docs
weight: 35000
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/idx_get/
---
## BuiltInDocumentProperties::idx_get method


根据属性名称返回一个 [DocumentProperty](../../documentproperty/) 对象。

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::BuiltInDocumentProperties::idx_get(System::String name) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | System::String | 要检索的属性名称（不区分大小写）。 |
## 备注


属性的字符串名称对应于可从 [BuiltInDocumentProperties](../) 获取的已键入属性的名称。

如果请求的属性在文档中不存在，但属性名称被识别为有效的内置名称，则会创建一个新的 [DocumentProperty](../../documentproperty/)，将其添加到集合中并返回。新创建的属性将根据内置属性的类型分配默认值（空字符串、零、**false** 或 DateTime.MinValue）。

如果请求的属性在文档中不存在且名称未被识别为内置名称，则返回 **null**。

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
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
