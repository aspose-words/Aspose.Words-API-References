---
title: "Aspose::Words::Tables::Table::SetBorders method"
linktitle: "SetBorders"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::SetBorders 方法。用 C++ 将所有表格边框设置为指定的线型、宽度和颜色。"
type: docs
weight: 69000
url: /zh/cpp/aspose.words.tables/table/setborders/
---
## Table::SetBorders method


将所有表格边框设置为指定的线型、宽度和颜色。

```cpp
void Aspose::Words::Tables::Table::SetBorders(Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| lineStyle | Aspose::Words::LineStyle | 要应用的线条样式。 |
| lineWidth | double | 要设置的线宽（单位为点）。 |
| color | System::Drawing::Color | 用于边框的颜色。 |

## 示例



展示如何在构建表格时应用边框和阴影颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 开始一个表格并为其边框设置默认颜色/粗细。
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// 创建一行，其中两个单元格具有不同的背景颜色。
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// 重置单元格格式以禁用背景颜色
// 为构建器创建的所有新单元格设置自定义边框粗细，
// 然后构建第二行。
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


展示如何一次性格式化表格的所有边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 清除表格中所有现有的边框。
table->ClearBorders();

// 设置一条绿色线作为此表格的所有外部和内部边框。
table->SetBorders(Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Table.SetBorders.docx");
```

## 另见

* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
