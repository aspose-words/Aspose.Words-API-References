---
title: "Aspose::Words::Markup::CustomXmlPropertyCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::CustomXmlPropertyCollection::idx_get 方法。获取 C++ 中具有指定名称的属性。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.markup/customxmlpropertycollection/idx_get/
---
## CustomXmlPropertyCollection::idx_get(const System::String\&) method


获取具有指定名称的属性。

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty> Aspose::Words::Markup::CustomXmlPropertyCollection::idx_get(const System::String &name)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 要定位的属性的区分大小写名称。 |

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

* Class [CustomXmlProperty](../../customxmlproperty/)
* Class [CustomXmlPropertyCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
## CustomXmlPropertyCollection::idx_get(int32_t) method


获取指定索引处的属性。

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty> Aspose::Words::Markup::CustomXmlPropertyCollection::idx_get(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 属性的零基索引。 |

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

* Class [CustomXmlProperty](../../customxmlproperty/)
* Class [CustomXmlPropertyCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
