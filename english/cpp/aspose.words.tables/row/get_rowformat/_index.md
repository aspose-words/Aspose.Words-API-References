---
title: get_RowFormat
second_title: Aspose.Words for C++ API Reference
description: Provides access to the formatting properties of the row.
type: docs
weight: 144
url: /cpp/aspose.words.tables/row/get_rowformat/
---
## Row::get_RowFormat method


Provides access to the formatting properties of the row.

```cpp
System::SharedPtr<Aspose::Words::Tables::RowFormat> Aspose::Words::Tables::Row::get_RowFormat()
```


## Examples



Shows how to modify the format of rows and cells in a table. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
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

// Use the first row's "RowFormat" property to modify the formatting
// of the contents of all cells in this row.
SharedPtr<RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Use the "CellFormat" property of the first cell in the last row to modify the formatting of that cell's contents.
SharedPtr<CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(ArtifactsDir + u"Table.RowCellFormat.docx");
```


Shows how to modify formatting of a table row. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");
SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Use the first row's "RowFormat" property to set formatting that modifies that entire row's appearance.
SharedPtr<Row> firstRow = table->get_FirstRow();
firstRow->get_RowFormat()->get_Borders()->set_LineStyle(LineStyle::None);
firstRow->get_RowFormat()->set_HeightRule(HeightRule::Auto);
firstRow->get_RowFormat()->set_AllowBreakAcrossPages(true);

doc->Save(ArtifactsDir + u"Table.RowFormat.docx");
```

## See Also

* Class [RowFormat](../../rowformat/)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
