---
title: "Aspose::Words::Lists::ListTemplate 枚举"
linktitle: "ListTemplate"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListTemplate 枚举。指定 Microsoft Word 在 C++ 中提供的预定义列表格式之一。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.lists/listtemplate/
---
## ListTemplate enum


指定 Microsoft Word 中可用的预定义列表格式之一。

```cpp
enum class ListTemplate
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| BulletDefault | 0 | 默认的项目符号列表，包含 9 级。第一级的项目符号是实心圆盘，第二级是空心圆， 第三级是方形。随后其余级别重复相同的格式。每一级相对于前一级向右缩进 0.25\"。对应 Microsoft Word 中“项目符号和编号”对话框的第一个项目符号列表模板。 |
| BulletDisk | n/a | 同 [BulletDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第一个项目符号列表模板。 |
| BulletCircle | n/a | 第一级的项目符号是圆形。其余级别与 [BulletDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第二个项目符号列表模板。 |
| BulletSquare | n/a | 第一级的项目符号是方形。其余级别与 [BulletDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第三个项目符号列表模板。 |
| BulletDiamonds | n/a | 第一级的项目符号是 4‑钻石 Wingding 字符。其余级别与 [BulletDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第五个项目符号列表模板。 |
| BulletArrowHead | n/a | 第一级的项目符号是箭头头部 Wingding 字符。其余级别与 [BulletDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第六个项目符号列表模板。 |
| BulletTick | n/a | 第一级的项目符号是勾选 Wingding 字符。其余级别与 [BulletDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第七个项目符号列表模板。 |
| NumberDefault | n/a | 默认的编号列表，包含 9 级。第一级使用阿拉伯数字编号 (1., 2., 3., ...)，第二级使用小写字母编号 (a., b., c., ...)，第三级使用小写罗马数字编号 (i., ii., iii., ...)。随后其余级别重复相同的格式。每一级相对于前一级向右缩进 0.25\"。对应 Microsoft Word 中“项目符号和编号”对话框的第一个编号列表模板。 |
| NumberArabicDot | n/a | 同 [NumberDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第一个编号列表模板。 |
| NumberArabicParenthesis | n/a | 第一级的编号为 \"1)\"。其余级别与 [NumberDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第二个编号列表模板。 |
| NumberUppercaseRomanDot | n/a | 第一级的编号为 \"I.\"。其余级别与 [NumberDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第三个编号列表模板。 |
| NumberUppercaseLetterDot | n/a | 第一级的编号为 \"A.\"。其余级别与 [NumberDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第四个编号列表模板。 |
| NumberLowercaseLetterParenthesis | n/a | 第一级的编号为 \"a)\"。其余级别与 [NumberDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第五个编号列表模板。 |
| NumberLowercaseLetterDot | n/a | 第一级的编号为 \"a.\"。其余级别与 [NumberDefault](./) 相同。对应 Microsoft Word 中“项目符号和编号”对话框的第六个编号列表模板。 |
| NumberLowercaseRomanDot | n/a | 第一层的编号是 "i."。其余层级与 [NumberDefault](./) 相同。对应于 Microsoft Word 中“项目符号和编号”对话框的第七个编号列表模板。 |
| OutlineNumbers | n/a | 一个大纲列表，其层级编号为 "1), a), i), (1), (a), (i), 1., a., i."。对应于 Microsoft Word 中“项目符号和编号”对话框的第一个大纲列表模板。 |
| OutlineLegal | n/a | 一个大纲列表，其层级编号为 "1., 1.1., 1.1.1, ..."。对应于 Microsoft Word 中“项目符号和编号”对话框的第二个大纲列表模板。 |
| OutlineBullets | n/a | 一个大纲列表，为不同层级提供各种项目符号。对应于 Microsoft Word 中“项目符号和编号”对话框的第三个大纲列表模板。 |
| OutlineHeadingsArticleSection | n/a | 一个大纲列表，其层级链接到标题样式。对应于 Microsoft Word 中“项目符号和编号”对话框的第四个大纲列表模板。 |
| OutlineHeadingsLegal | n/a | 一个大纲列表，其层级链接到标题样式。对应于 Microsoft Word 中“项目符号和编号”对话框的第五个大纲列表模板。 |
| OutlineHeadingsNumbers | n/a | 一个大纲列表，其层级链接到标题样式。对应于 Microsoft Word 中“项目符号和编号”对话框的第六个大纲列表模板。 |
| OutlineHeadingsChapter | n/a | 一个大纲列表，其层级链接到标题样式。对应于 Microsoft Word 中“项目符号和编号”对话框的第七个大纲列表模板。 |

## 备注


列表模板值作为参数传递给 [Add()](../listcollection/add/) 方法。

Aspose.Words 列表模板对应于 Microsoft Word 2003 中“项目符号和编号”对话框提供的 21 种列表模板。

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
