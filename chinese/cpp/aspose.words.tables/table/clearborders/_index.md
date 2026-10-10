---
title: "Aspose::Words::Tables::Table::ClearBorders 方法"
linktitle: "ClearBorders"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::ClearBorders 方法。移除此表在 C++ 中的所有表格和单元格边框。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.tables/table/clearborders/
---
## Table::ClearBorders method


移除此表格上所有的表格和单元格边框。

```cpp
void Aspose::Words::Tables::Table::ClearBorders()
```


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


展示如何从表格中移除所有边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Hello world!");
builder->EndTable();

// 修改顶部边框的颜色和粗细。
System::SharedPtr<Aspose::Words::Border> topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Double, 1.5, System::Drawing::Color::get_Red(), true);

ASPOSE_ASSERT_EQ(1.5, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Double, topBorder->get_LineStyle());

// 清除表格中所有单元格的边框，然后保存文档。
table->ClearBorders();
doc->Save(get_ArtifactsDir() + u"Table.ClearBorders.docx");

// 重新打开文档后，验证表格属性的值。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Table.ClearBorders.docx");
table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(Aspose::Words::BorderType::Top);

ASPOSE_ASSERT_EQ(0.0, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::None, topBorder->get_LineStyle());
```

## 另见

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
