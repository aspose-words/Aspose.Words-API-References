---
title: "Aspose::Words::Lists::List::get_IsListStyleReference 方法"
linktitle: "get_IsListStyleReference"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::List::get_IsListStyleReference 方法。若此列表是对列表样式的引用，则在 C++ 中返回 true。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.lists/list/get_isliststylereference/
---
## List::get_IsListStyleReference method


如果此列表是列表样式的引用，则返回 **true**。

```cpp
bool Aspose::Words::Lists::List::get_IsListStyleReference()
```

## 备注


注意，修改引用列表样式的列表属性不会产生效果。列表样式本身指定的列表格式始终具有最高优先级。

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

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
