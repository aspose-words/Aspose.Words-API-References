---
title: "Aspose::Words::Tables::Cell::get_CellFormat 方法"
linktitle: "get_CellFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Cell::get_CellFormat 方法。提供对单元格格式属性的访问（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.tables/cell/get_cellformat/
---
## Cell::get_CellFormat method


提供对单元格格式属性的访问。

```cpp
System::SharedPtr<Aspose::Words::Tables::CellFormat> Aspose::Words::Tables::Cell::get_CellFormat()
```


## 示例



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


展示如何将两个表的行合并为一个。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// 下面是从文档中获取表的两种方法。
// 1 -  来自 Body 节点的 "Tables" 集合：
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 - 使用 "GetChild" 方法：
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// 将当前表格的所有行追加到下一个表格。
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// 移除空的表格容器。
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## 另见

* Class [CellFormat](../../cellformat/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
