---
title: "Aspose::Words::Lists::ListFormat 类"
linktitle: "ListFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListFormat 类。允许控制应用于段落的列表格式。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.lists/listformat/
---
## ListFormat class


允许控制对段落应用的列表格式。要了解更多信息，请访问 [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/) 文档文章。

```cpp
class ListFormat : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ApplyBulletDefault](./applybulletdefault/)() | 启动一个新的默认项目符号列表并将其应用于段落。 |
| [ApplyNumberDefault](./applynumberdefault/)() | 启动一个新的默认编号列表并将其应用于段落。 |
| [get_IsListItem](./get_islistitem/)() | 当段落已应用项目符号或编号格式时为 True。 |
| [get_List](./get_list/)() | 获取或设置此段落所属的列表。 |
| [get_ListLevel](./get_listlevel/)() | 返回列表级别格式以及应用于当前段落的任何格式覆盖。 |
| [get_ListLevelNumber](./get_listlevelnumber/)() | 获取或设置段落的列表级别编号（0 到 8）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ListIndent](./listindent/)() | 将当前段落的列表级别提升一级。 |
| [ListOutdent](./listoutdent/)() | 将当前段落的列表级别降低一级。 |
| [RemoveNumbers](./removenumbers/)() | 从当前段落移除编号或项目符号，并将列表级别设为零。 |
| [set_List](./set_list/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | 用于设置 [Aspose::Words::Lists::ListFormat::get_List](./get_list/) 的 setter。 |
| [set_ListLevelNumber](./set_listlevelnumber/)(int32_t) | 用于设置 [Aspose::Words::Lists::ListFormat::get_ListLevelNumber](./get_listlevelnumber/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


Microsoft Word 文档中的段落可以使用项目符号或编号。当段落使用项目符号或编号时，称为已对段落应用列表格式。

您不能直接创建 [ListFormat](./) 类的对象。您通过另一个可以关联列表格式的对象的属性来访问 [ListFormat](./)。目前可以拥有列表格式的对象有：[Paragraph](../../aspose.words/paragraph/)、[Style](../../aspose.words/style/) 和 [DocumentBuilder](../../aspose.words/documentbuilder/)。

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

列表格式本身存储在一个与段落分离的 [List](../list/) 对象中。列表对象存储在 [ListCollection](../listcollection/) 集合中。每个 [Document](../../aspose.words/document/) 只有一个 [ListCollection](../listcollection/) 集合。

段落并不实际属于某个列表。段落仅通过 [List](./get_list/) 属性引用特定的列表对象，并通过 [ListLevelNumber](./get_listlevelnumber/) 属性引用列表中的特定级别。通过设置这两个属性，您可以控制段落应用的项目符号和编号。

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

## 另见

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
