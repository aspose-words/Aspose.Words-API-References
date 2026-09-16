---
title: "Aspose::Words::Properties::CustomDocumentProperties class"
linktitle: "CustomDocumentProperties"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::CustomDocumentProperties class. 自定义文档属性的集合。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class


自定义文档属性的集合。要了解更多信息，请访问 [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) 文档文章。

```cpp
class CustomDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | 创建一个新的自定义文档属性，数据类型为 [String](../propertytype/)。 |
| [Add](./add/)(const System::String\&, int32_t) | 创建一个新的自定义文档属性，数据类型为 [Number](../propertytype/)。 |
| [Add](./add/)(const System::String\&, System::DateTime) | 创建一个新的自定义文档属性，数据类型为 [DateTime](../propertytype/)。 |
| [Add](./add/)(const System::String\&, bool) | 创建一个新的自定义文档属性，数据类型为 [Boolean](../propertytype/)。 |
| [Add](./add/)(const System::String\&, double) | 创建一个新的自定义文档属性，数据类型为 [Double](../propertytype/)。 |
| [AddLinkToContent](./addlinktocontent/)(const System::String\&, const System::String\&) | 创建一个新的链接到内容的自定义文档属性。 |
| [Clear](../documentpropertycollection/clear/)() | 从集合中移除所有属性。 |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | 如果集合中存在具有指定名称的属性，则返回 **true**。 |
| [get_Count](../documentpropertycollection/get_count/)() | 获取集合中项目的数量。 |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | 返回一个可用于遍历集合中所有项的枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](../documentpropertycollection/idx_get/)(System::String) | 根据属性名称返回一个 [DocumentProperty](../documentproperty/) 对象。 |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | 根据索引返回一个 [DocumentProperty](../documentproperty/) 对象。 |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | 根据名称获取属性的索引。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | 从集合中移除具有指定名称的属性。 |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | 移除指定索引处的属性。 |
| static [Type](./type/)() |  |
## 备注


每个 [DocumentProperty](../documentproperty/) 对象表示容器文档的自定义属性。

属性名称不区分大小写。

集合中的属性按名称字母顺序排序。

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

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
