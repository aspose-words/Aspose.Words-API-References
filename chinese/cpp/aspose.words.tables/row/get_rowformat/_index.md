---
title: "Aspose::Words::Tables::Row::get_RowFormat 方法"
linktitle: "get_RowFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Row::get_RowFormat 方法。提供对 C++ 中行的格式属性的访问。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.tables/row/get_rowformat/
---
## Row::get_RowFormat method


提供对行的格式属性的访问。

```cpp
System::SharedPtr<Aspose::Words::Tables::RowFormat> Aspose::Words::Tables::Row::get_RowFormat()
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

* Class [RowFormat](../../rowformat/)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
