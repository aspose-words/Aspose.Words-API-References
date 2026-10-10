---
title: "Aspose::Words::Lists::ListFormat::get_ListLevelNumber 方法"
linktitle: "get_ListLevelNumber"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListFormat::get_ListLevelNumber 方法。获取或设置段落的列表级别编号（0 到 8），适用于 C++。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.lists/listformat/get_listlevelnumber/
---
## ListFormat::get_ListLevelNumber method


获取或设置段落的列表级别编号（0 到 8）。

```cpp
int32_t Aspose::Words::Lists::ListFormat::get_ListLevelNumber()
```

## 备注


在 Word 文档中，列表可能包含 1 或 9 级，编号为 0 到 8。

仅当 [List](../get_list/) 属性设置为引用有效列表时才有效。

## 示例



展示如何创建项目符号列表和编号列表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
// 我们可以通过增加缩进级别来创建嵌套列表。
// 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
// 我们在列表开始和结束之间添加的每个段落都会成为列表中的一项。
// 下面是使用文档生成器可以创建的两种列表类型。
// 1 -  项目符号列表：
// 此列表将在每个段落前应用缩进和项目符号（"•"）。
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// 结束项目符号列表。
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  编号列表：
// 编号列表通过为每个项目编号，为段落创建逻辑顺序。
builder->get_ListFormat()->ApplyNumberDefault();

// 此段落是第一项。编号列表的第一项的列表符号将是 "1."。
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// 调用 "ListIndent" 方法以增加当前列表级别，
// 这将在第一级列表的当前项处启动一个新的独立列表，具有更深的缩进。
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// 以下是第二级列表的前三个列表项，它们将保持计数
// 独立于第一级列表的计数。根据当前的列表格式，
// 它们的符号将是 "a.", "b.", 和 "c."。
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// 调用 "ListOutdent" 方法返回到上一级列表。
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// 这两个段落将继续第一级列表的计数。
// 这些项的符号将是 "2.", 和 "3."
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// 如果我们将列表级别提升到之前已添加项目的级别，
// 嵌套列表将与之前的列表分离，并且其编号将从头开始。
// 这些列表项的符号将是 "a.", "b.", "c.", "d.", 和 "e"。
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// 再次减少列表级别。
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// 结束编号列表。
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


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

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
