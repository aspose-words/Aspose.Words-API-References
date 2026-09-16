---
title: "Aspose::Words::Tables::CellFormat::get_PreferredWidth 方法"
linktitle: "get_PreferredWidth"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::CellFormat::get_PreferredWidth 方法。返回或设置单元格的首选宽度（C++）。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.tables/cellformat/get_preferredwidth/
---
## CellFormat::get_PreferredWidth method


返回或设置单元格的首选宽度。

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::CellFormat::get_PreferredWidth()
```

## 备注


首选宽度（以及表格的自动适应选项）决定表格布局算法如何计算单元格的实际宽度。[Table](../../table/) 布局可以在 Aspose.Words 保存文档时执行，或在 Microsoft Word 显示文档时执行。

首选宽度可以以点或百分比指定。首选宽度也可以指定为 "auto"，这表示未指定首选宽度。

默认值是 [Auto](../../preferredwidth/auto/)。

## 示例



展示如何为表格单元格设置首选宽度。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// 有两种方式将 "PreferredWidth" 类应用于表格单元格。
// 1 - 基于点数设置绝对首选宽度：
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 - 基于表格宽度的百分比设置相对首选宽度：
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// 未指定首选宽度的单元格将占用剩余的可用空间。
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// 每次对 "PreferredWidth" 属性的配置都会创建一个新对象。
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## 另见

* Class [PreferredWidth](../../preferredwidth/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
