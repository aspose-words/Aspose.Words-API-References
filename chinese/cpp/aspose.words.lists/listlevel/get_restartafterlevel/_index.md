---
title: "Aspose::Words::Lists::ListLevel::get_RestartAfterLevel 方法"
linktitle: "get_RestartAfterLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListLevel::get_RestartAfterLevel 方法。设置或返回在指定列表级别重新开始编号之前必须出现的列表级别（在 C++ 中）。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.lists/listlevel/get_restartafterlevel/
---
## ListLevel::get_RestartAfterLevel method


设置或返回在指定列表级别重新开始编号之前必须出现的列表级别。

```cpp
int32_t Aspose::Words::Lists::ListLevel::get_RestartAfterLevel() const
```

## 备注


-1 的值表示编号将继续。

## 示例



展示自定义列表标签的高级方法。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
// 我们可以通过增加缩进级别来创建嵌套列表。
// 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
// 我们在列表开始和结束之间添加的每个段落都会成为列表中的一项。
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// 第 1 级标签将根据 "Heading 1" 段落样式进行格式化，并带有前缀。
// 这些将显示为 "Appendix A"、 "Appendix B"……
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"Appendix \x0000");
list->get_ListLevels()->idx_get(0)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);
list->get_ListLevels()->idx_get(0)->set_LinkedStyle(doc->get_Styles()->idx_get(u"Heading 1"));

// 第 2 级标签将显示第一和第二列表级别的当前编号，并带有前导零。
// 如果第一列表级别为 1，则这些列表标签将显示为 "Section (1.01)"、 "Section (1.02)"……
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"Section (\x0000" u".\x0001" u")");
list->get_ListLevels()->idx_get(1)->set_NumberStyle(Aspose::Words::NumberStyle::LeadingZero);

// 请注意，更高级别使用 UppercaseLetter 编号。
// 我们可以设置 "IsLegal" 属性，以在更高级别的列表中使用阿拉伯数字。
list->get_ListLevels()->idx_get(1)->set_IsLegal(true);
list->get_ListLevels()->idx_get(1)->set_RestartAfterLevel(0);

// 第 3 级标签将使用大写罗马数字，并带有前缀和后缀，并将在每个 List 第 1 级项目处重新开始。
// 这些列表标签将类似于 "-I-", "-II-"...
list->get_ListLevels()->idx_get(2)->set_NumberFormat(u"-\x0002" u"-");
list->get_ListLevels()->idx_get(2)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
list->get_ListLevels()->idx_get(2)->set_RestartAfterLevel(1);

// 将所有列表级别的标签加粗。
for (auto&& level : list->get_ListLevels())
{
    level->get_Font()->set_Bold(true);
}

// 将列表格式应用于当前段落。
builder->get_ListFormat()->set_List(list);

// 创建列表项，以显示我们所有三个列表级别。
for (int32_t n = 0; n < 2; n++)
{
    for (int32_t i = 0; i < 3; i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(System::String(u"Level ") + i);
    }
}

builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.CreateListRestartAfterHigher.docx");
```

## 另见

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
