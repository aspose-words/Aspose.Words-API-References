---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection 类"
linktitle: "CustomXmlSchemaCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection 类。一个字符串集合，表示与自定义 XML 部分关联的 XML 架构。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class


一组表示与自定义 XML 部件关联的 XML 架构的字符串。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。

```cpp
class CustomXmlSchemaCollection : public System::Collections::Generic::IEnumerable<System::String>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::String\&) | 向集合中添加一个项。 |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | 从集合中移除所有元素。 |
| [Clone](./clone/)() | 对该对象进行深度克隆。 |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | 获取集合中包含的元素数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个可用于遍历集合中所有项的枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 获取或设置指定索引处的元素。 |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | 获取或设置指定索引处的元素。 |
| [IndexOf](./indexof/)(const System::String\&) | 返回集合中指定值的零基索引。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | 从集合中移除指定的值。 |
| [RemoveAt](./removeat/)(int32_t) | 在指定索引处移除一个值。 |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| 类型定义 | 描述 |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## 备注


您不能创建此类的实例。您可以通过 [Schemas](../customxmlpart/get_schemas/) 属性访问自定义 XML 部分的 XML 架构集合。

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
