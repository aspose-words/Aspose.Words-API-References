---
title: "Aspose::Words::Markup::CustomXmlPropertyCollection 类"
linktitle: "CustomXmlPropertyCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::CustomXmlPropertyCollection 类。表示自定义 XML 属性或智能标签属性的集合。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class


表示一组自定义 XML 属性或智能标签属性。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。

```cpp
class CustomXmlPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlProperty\>\&) | 向集合中添加属性。 |
| [Clear](./clear/)() | 从集合中移除所有元素。 |
| [Contains](./contains/)(const System::String\&) | 确定集合是否包含具有给定名称的属性。 |
| [get_Count](./get_count/)() | 获取集合中包含的元素数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个可用于遍历集合中所有项的枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | 获取具有指定名称的属性。 |
| [idx_get](./idx_get/)(int32_t) | 获取指定索引处的属性。 |
| [IndexOfKey](./indexofkey/)(const System::String\&) | 返回集合中指定属性的零基索引。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | 从集合中移除具有指定名称的属性。 |
| [RemoveAt](./removeat/)(int32_t) | 移除指定索引处的属性。 |
| static [Type](./type/)() |  |
## 备注


项为 [CustomXmlProperty](../customxmlproperty/) 对象。

## 示例



展示如何使用智能标签属性获取有关智能标签的深入信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

// 当 Microsoft Word 在文档中识别其文本的一部分为某种数据时，会出现智能标签，
// 例如名称、日期或地址，并将其转换为显示紫色点状下划线的超链接。
// 在 Word 2003 中，我们可以通过 "Tools" -> "AutoCorrect options..." -> "SmartTags" 来启用智能标签。
// 在我们的输入文档中，有三个对象被 Microsoft Word 注册为智能标签。
// 智能标签可能是嵌套的，因此此集合包含更多。
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag> >()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// 智能标签的 "Properties" 成员包含其元数据，不同类型的智能标签会有所不同。
// "date" 类型智能标签的属性包含其年份、月份和日期。
System::SharedPtr<Aspose::Words::Markup::CustomXmlPropertyCollection> properties = smartTags[7]->get_Properties();

ASSERT_EQ(4, properties->get_Count());

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Property name: {0}, value: {1}", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Value()) << std::endl;
        ASSERT_EQ(u"", enumerator->get_Current()->get_Uri());
    }
}

// 我们还可以通过多种方式访问这些属性，例如键值对。
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// 下面是从属性集合中移除元素的三种方法。
// 1 -  按索引删除：
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  按名称删除：
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 - 一次性清除整个集合：
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## 另见

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
