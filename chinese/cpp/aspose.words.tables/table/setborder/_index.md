---
title: "Aspose::Words::Tables::Table::SetBorder 方法"
linktitle: "SetBorder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::SetBorder 方法。将指定的表边框设置为 C++ 中指定的线型、宽度和颜色。"
type: docs
weight: 68000
url: /zh/cpp/aspose.words.tables/table/setborder/
---
## Table::SetBorder method


将指定的表格边框设置为指定的线型、宽度和颜色。

```cpp
void Aspose::Words::Tables::Table::SetBorder(Aspose::Words::BorderType borderType, Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color, bool isOverrideCellBorders)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | 要更改的表格边框。 |
| lineStyle | Aspose::Words::LineStyle | 要应用的线条样式。 |
| lineWidth | double | 要设置的线宽（单位为点）。 |
| color | System::Drawing::Color | 用于边框的颜色。 |
| isOverrideCellBorders | bool | 当 **true** 时，会删除所有现有的显式单元格边框。 |

## 示例



展示如何对表格应用外框边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 将表格对齐到页面中心。
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// 清除表格中所有现有的边框和阴影。
table->ClearBorders();
table->ClearShading();

// 为表格的外框添加绿色边框。
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// 用浅绿色实色填充单元格。
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## 另见

* Enum [BorderType](../../../aspose.words/bordertype/)
* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
