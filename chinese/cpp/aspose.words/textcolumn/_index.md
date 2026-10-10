---
title: "Aspose::Words::TextColumn 类"
linktitle: "TextColumn"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextColumn 类。表示单个文本列。TextColumn 是 TextColumnCollection 集合的成员。TextColumn 集合包含文档节中的所有列。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 70000
url: /zh/cpp/aspose.words/textcolumn/
---
## TextColumn class


表示单个文本列。 [TextColumn](./) 是 [TextColumnCollection](../textcolumncollection/) 集合的成员。 [TextColumn](./) 集合包含文档节中的所有列。欲了解更多，请访问 [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) 文档文章。

```cpp
class TextColumn : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_SpaceAfter](./get_spaceafter/)() | 获取或设置此列与下一列之间的间距（单位为点）。最后一列不需要此设置。 |
| [get_Width](./get_width/)() | 获取或设置文本列的宽度（单位为点）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SpaceAfter](./set_spaceafter/)(double) | 用于设置 [Aspose::Words::TextColumn::get_SpaceAfter](./get_spaceafter/) 的 setter。 |
| [set_Width](./set_width/)(double) | 用于设置 [Aspose::Words::TextColumn::get_Width](./get_width/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[EvenlySpaced](../textcolumncollection/get_evenlyspaced/) to **true**.

当创建新的 [TextColumn](./) 时，其宽度和间距均设置为零。

## 示例



展示如何创建间距不均匀的列。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// 确定用于排列列的可用空间量。
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// 将第一列设为窄列。
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// 将第二列设为占据页面页边距内剩余的全部空间。
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
