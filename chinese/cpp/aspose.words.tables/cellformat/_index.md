---
title: "Aspose::Words::Tables::CellFormat 类"
linktitle: "CellFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::CellFormat 类。表示表格单元格的所有格式设置。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.tables/cellformat/
---
## CellFormat class


表示表格单元格的全部格式。要了解更多信息，请访问 [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) 文档文章。

```cpp
class CellFormat : public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | 重置为默认单元格格式。不会更改单元格的宽度。 |
| [get_Borders](./get_borders/)() | 获取单元格的边框集合。 |
| [get_BottomPadding](./get_bottompadding/)() | 返回或设置在单元格内容下方添加的空间量（以点为单位）。 |
| [get_FitText](./get_fittext/)() | 如果 **true**，则使文本适应单元格，将每个段落压缩到单元格的宽度。 |
| [get_HideMark](./get_hidemark/)() | 返回单元格标记的可见性。 |
| [get_HorizontalMerge](./get_horizontalmerge/)() | 指定单元格在行中如何水平合并到其他单元格。 |
| [get_LeftPadding](./get_leftpadding/)() | 返回或设置在单元格内容左侧添加的空间量（以点为单位）。 |
| [get_Orientation](./get_orientation/)() | 返回或设置表格单元格中文本的方向。 |
| [get_PreferredWidth](./get_preferredwidth/)() | 返回或设置单元格的首选宽度。 |
| [get_RightPadding](./get_rightpadding/)() | 返回或设置在单元格内容右侧添加的空间量（以点为单位）。 |
| [get_Shading](./get_shading/)() | 返回一个指向单元格阴影格式的 [Shading](../../aspose.words/shading/) 对象。 |
| [get_TopPadding](./get_toppadding/)() | 返回或设置在单元格内容上方添加的空间量（以点为单位）。 |
| [get_VerticalAlignment](./get_verticalalignment/)() | 返回或设置单元格中文本的垂直对齐方式。 |
| [get_VerticalMerge](./get_verticalmerge/)() | 指定单元格如何垂直合并到其他单元格。 |
| [get_Width](./get_width/)() | 获取单元格的宽度（以点为单位）。 |
| [get_WrapText](./get_wraptext/)() | 如果 **true**，则对单元格进行文本换行。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | 设置器用于 [Aspose::Words::Tables::CellFormat::get_BottomPadding](./get_bottompadding/)。 |
| [set_FitText](./set_fittext/)(bool) | 设置器用于 [Aspose::Words::Tables::CellFormat::get_FitText](./get_fittext/)。 |
| [set_HideMark](./set_hidemark/)(bool) | 设置单元格标记的可见性。 |
| [set_HorizontalMerge](./set_horizontalmerge/)(Aspose::Words::Tables::CellMerge) | 设置器用于 [Aspose::Words::Tables::CellFormat::get_HorizontalMerge](./get_horizontalmerge/)。 |
| [set_LeftPadding](./set_leftpadding/)(double) | 设置器用于 [Aspose::Words::Tables::CellFormat::get_LeftPadding](./get_leftpadding/)。 |
| [set_Orientation](./set_orientation/)(Aspose::Words::TextOrientation) | 设置器用于 [Aspose::Words::Tables::CellFormat::get_Orientation](./get_orientation/)。 |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | 设置器用于 [Aspose::Words::Tables::CellFormat::get_PreferredWidth](./get_preferredwidth/)。 |
| [set_RightPadding](./set_rightpadding/)(double) | 设置器用于 [Aspose::Words::Tables::CellFormat::get_RightPadding](./get_rightpadding/)。 |
| [set_TopPadding](./set_toppadding/)(double) | 设置器用于 [Aspose::Words::Tables::CellFormat::get_TopPadding](./get_toppadding/)。 |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | 用于设置 [Aspose::Words::Tables::CellFormat::get_VerticalAlignment](./get_verticalalignment/) 的 setter。 |
| [set_VerticalMerge](./set_verticalmerge/)(Aspose::Words::Tables::CellMerge) | 用于设置 [Aspose::Words::Tables::CellFormat::get_VerticalMerge](./get_verticalmerge/) 的 setter。 |
| [set_Width](./set_width/)(double) | 用于设置 [Aspose::Words::Tables::CellFormat::get_Width](./get_width/) 的 setter。 |
| [set_WrapText](./set_wraptext/)(bool) | 用于设置 [Aspose::Words::Tables::CellFormat::get_WrapText](./get_wraptext/) 的 setter。 |
| [SetPaddings](./setpaddings/)(double, double, double, double) | 设置要在单元格内容的左/上/右/下添加的空间量（以点为单位）。 |
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


展示如何修改表格单元格的格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// 使用单元格的 "CellFormat" 属性来设置修改该单元格外观的格式。
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(get_ArtifactsDir() + u"Table.CellFormat.docx");
```

## 另见

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
