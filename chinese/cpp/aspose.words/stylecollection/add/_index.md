---
title: "Aspose::Words::StyleCollection::Add method"
linktitle: "Add"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::StyleCollection::Add method. 在 C++ 中创建一个新的用户定义样式并将其添加到集合中。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/stylecollection/add/
---
## StyleCollection::Add method


创建一个新的用户自定义样式并将其添加到集合中。

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::Add(Aspose::Words::StyleType type, const System::String &name)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| type | Aspose::Words::StyleType | 一个指定要创建的样式类型的 [StyleType](../../styletype/) 值。 |
| name | const System::String\& | 创建样式时区分大小写的名称。 |
## 备注


您可以创建字符、段落或列表样式。

创建列表样式时，样式会使用默认的编号列表格式 (1 \\ a \\ i)。

如果已存在同名样式，则抛出异常。

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


展示如何向文档的样式集合添加一个 [Style](../../style/)。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// 为我们以后可能添加到此集合的新样式设置默认参数。
styles->get_DefaultFont()->set_Name(u"Courier New");
// 如果我们添加一个 \"StyleType.Paragraph\" 类型的样式，集合将应用这些值。
// 其 \"DefaultParagraphFormat\" 属性到样式的 \"ParagraphFormat\" 属性。
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// 添加一个样式，然后验证它具有默认设置。
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## 另见

* Class [Style](../../style/)
* Enum [StyleType](../../styletype/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
