---
title: "Aspose::Words::Tables::RowFormat 类"
linktitle: "RowFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::RowFormat 类。表示表格行的所有格式。要了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.tables/rowformat/
---
## RowFormat class


表示表格行的全部格式。要了解更多信息，请访问 [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) 文档文章。

```cpp
class RowFormat : public Aspose::Words::IBorderAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | 重置为默认的行格式。 |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | 如果允许表格行中的文本在分页符处拆分，则为 True。 |
| [get_Borders](./get_borders/)() | 获取该行默认单元格边框的集合。 |
| [get_HeadingFormat](./get_headingformat/)() | 如果表格跨越多页时，行在每页上作为表格标题重复，则为 True。 |
| [get_Height](./get_height/)() | 获取或设置表格行的高度（单位为点）。 |
| [get_HeightRule](./get_heightrule/)() | 获取或设置确定表格行高度的规则。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | 设置器用于 [Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)。 |
| [set_HeadingFormat](./set_headingformat/)(bool) | 设置器用于 [Aspose::Words::Tables::RowFormat::get_HeadingFormat](./get_headingformat/)。 |
| [set_Height](./set_height/)(double) | 设置器用于 [Aspose::Words::Tables::RowFormat::get_Height](./get_height/)。 |
| [set_HeightRule](./set_heightrule/)(Aspose::Words::HeightRule) | 设置器用于 [Aspose::Words::Tables::RowFormat::get_HeightRule](./get_heightrule/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何使用自定义边框构建表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// 为文档生成器设置表格格式选项
// 它们将应用于我们使用它添加的每一行和每个单元格。
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// 更改格式将应用于当前单元格，
// 以及随后使用生成器创建的任何新单元格。
// 这不会影响我们之前添加的单元格。
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// 增加行高以适应竖排文本。
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


展示如何修改表格中行和单元格的格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// 使用第一行的 "RowFormat" 属性来修改格式
// 该行所有单元格内容的格式。
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// 使用最后一行中第一个单元格的 "CellFormat" 属性来修改该单元格内容的格式。
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


展示如何修改表格行的格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 使用第一行的 "RowFormat" 属性设置格式，以修改整行的外观。
System::SharedPtr<Aspose::Words::Tables::Row> firstRow = table->get_FirstRow();
firstRow->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::None);
firstRow->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
firstRow->get_RowFormat()->set_AllowBreakAcrossPages(true);

doc->Save(get_ArtifactsDir() + u"Table.RowFormat.docx");
```

## 另见

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
