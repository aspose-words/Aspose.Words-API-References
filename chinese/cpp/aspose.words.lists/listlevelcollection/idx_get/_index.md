---
title: "Aspose::Words::Lists::ListLevelCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListLevelCollection::idx_get 方法。根据索引获取列表级别（C++）。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.lists/listlevelcollection/idx_get/
---
## ListLevelCollection::idx_get method


通过索引获取列表级别。

```cpp
System::SharedPtr<Aspose::Words::Lists::ListLevel> Aspose::Words::Lists::ListLevelCollection::idx_get(int32_t index)
```


## 示例



展示在使用 [DocumentBuilder](../../../aspose.words/documentbuilder/) 时如何对段落应用自定义列表格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
// 我们可以通过增加缩进级别来创建嵌套列表。
// 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
// 我们在列表开始和结束之间添加的每个段落都会成为列表中的一项。
// 从 Microsoft Word 模板创建列表，并自定义其前两个列表级别。
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// 此 NumberFormat 值将生成星形项目符号列表符号。
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// 创建段落并将我们自定义列表格式的两个级别应用于这些段落。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```


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

* Class [ListLevel](../../listlevel/)
* Class [ListLevelCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
