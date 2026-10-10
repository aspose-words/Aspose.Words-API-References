---
title: "Aspose::Words::Lists::ListCollection 类"
linktitle: "ListCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListCollection 类。存储并管理文档中使用的项目符号和编号列表的格式。欲了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.lists/listcollection/
---
## ListCollection class


存储并管理文档中使用的项目符号和编号列表的格式。要了解更多信息，请访问 [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/) 文档文章。

```cpp
class ListCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(Aspose::Words::Lists::ListTemplate) | 基于预定义模板创建一个新列表，并将其添加到文档中的列表集合中。 |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | 创建一个引用列表样式的新列表，并将其添加到文档中的列表集合中。 |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | 通过复制指定的列表创建一个新列表，并将其添加到文档中的列表集合中。 |
| [AddSingleLevelList](./addsinglelevellist/)(Aspose::Words::Lists::ListTemplate) | 基于预定义模板创建一个新的单层列表，并将其添加到文档的列表集合中。 |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | 获取文档中编号列表和项目符号列表的数量。 |
| [get_Document](./get_document/)() const | 获取所属文档。 |
| [GetEnumerator](./getenumerator/)() override | 获取将在文档中枚举列表的枚举器对象。 |
| [GetListByListId](./getlistbylistid/)(int32_t) | 通过列表标识符获取列表。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 通过索引获取列表。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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


Microsoft Word 文档中的列表是一组列表格式属性。列表的格式存储在 [ListCollection](./) 集合中，独立于文本段落。

您不能创建此类的对象。每个文档始终只有一个 [ListCollection](./) 对象，可通过 [Lists](../../aspose.words/documentbase/get_lists/) 属性访问。

要基于预定义的列表模板或列表样式创建新列表，请使用 [Add()](../) 方法。

要创建格式与现有列表完全相同的新列表，请使用 [AddCopy()](../) 方法。

要使段落呈现项目符号或编号，需要通过将 [List](../list/) 对象分配给 [ListFormat](../listformat/) 的 [List](../listformat/get_list/) 属性来对段落应用列表格式。

要从段落中移除列表格式，请使用 [RemoveNumbers](../listformat/removenumbers/) 方法。

如果您对 WordprocessingML 有一些了解，您可能知道它为 “list” 与 “list definition” 定义了不同的概念。这正对应于低层次上 Microsoft Word 文档中列表格式的存储方式。[List](../list/) 定义类似于 “模式”，而列表则类似于列表定义的实例。

为了简化编程模型，Aspose.Words 以类似于 Microsoft Word 在用户界面中隐藏此区别的方式，隐藏了列表与列表定义之间的差异。这使您可以更专注于文档的外观，而无需构建低层对象来满足 Microsoft Word 文件格式的要求。

在当前版本的 [Aspose.Words](../../aspose.words/) 中，列表创建后无法删除。这类似于 Microsoft Word，用户无法对列表定义进行显式控制。

## 示例



展示如何使用列表级别。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
// 我们可以通过增加缩进级别来创建嵌套列表。
// 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
// 我们在列表开始和结束之间添加的每个段落都会成为列表中的一项。
// 下面是使用文档生成器可以创建的两种列表类型。
// 1 -  编号列表：
// 编号列表通过为每个项目编号，为段落创建逻辑顺序。
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// 通过设置 "ListLevelNumber" 属性，我们可以增加列表级别
// 在当前列表项处开始一个独立的子列表。
// Microsoft Word 列表模板 "NumberDefault" 使用数字来创建第一列表级别的列表层级。
// 更深的列表级别使用字母和小写罗马数字。
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  一个项目符号列表：
// 此列表将在每个段落前应用缩进和项目符号（"•"）。
// 此列表的更深层级将使用不同的符号，例如 "■" 和 "○"。
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 我们可以通过取消设置 "List" 标志来禁用列表格式，从而不将后续段落格式化为列表。
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


演示如何通过复制列表来重新开始列表编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
// 我们可以通过增加缩进级别来创建嵌套列表。
// 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
// 我们在列表开始和结束之间添加的每个段落都会成为列表中的一项。
// 从 Microsoft Word 模板创建列表，并自定义其第一个列表级别。
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// 将我们的列表应用于一些段落。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// 我们可以将现有列表的副本添加到文档的列表集合中
// 以创建一个相似的列表而不更改原始列表。
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// 将第二个列表应用于新段落。
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## 另见

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
