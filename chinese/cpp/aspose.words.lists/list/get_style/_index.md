---
title: "Aspose::Words::Lists::List::get_Style 方法"
linktitle: "get_Style"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::List::get_Style 方法。获取此列表在 C++ 中引用或定义的列表样式。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.lists/list/get_style/
---
## List::get_Style method


获取此列表引用或定义的列表样式。

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Lists::List::get_Style()
```

## 备注


如果此列表未关联到列表样式，属性将返回 **null**。

列表可能是对列表样式的引用，在这种情况下，[IsListStyleReference](../get_isliststylereference/) 将为 **true**。

列表也可能是列表样式的定义，在这种情况下，[IsListStyleDefinition](../get_isliststyledefinition/) 将为 **true**。此类列表不能直接应用于文档中的段落。

## 示例



展示如何创建列表样式并在文档中使用它。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
// 我们可以通过增加缩进级别来创建嵌套列表。
// 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
// 我们在列表开始和结束之间添加的每个段落都会成为列表中的一项。
// 我们可以在样式中包含整个 List 对象。
System::SharedPtr<Aspose::Words::Style> listStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle");

System::SharedPtr<Aspose::Words::Lists::List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// 更改我们列表中所有列表级别的外观。
for (auto&& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// 从样式中的列表创建另一个列表。
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// 添加一些我们的列表将格式化的列表项。
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// 创建并应用基于列表样式的另一个列表。
System::SharedPtr<Aspose::Words::Lists::List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateAndUseListStyle.docx");
```

## 另见

* Class [Style](../../../aspose.words/style/)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
