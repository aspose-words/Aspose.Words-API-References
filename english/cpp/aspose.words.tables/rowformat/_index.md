---
title: Aspose::Words::Tables::RowFormat class
linktitle: RowFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::RowFormat class. Represents all formatting for a table row. To learn more, visit the  documentation article in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.tables/rowformat/
---
## RowFormat class


Represents all formatting for a table row. To learn more, visit the [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) documentation article.

```cpp
class RowFormat : public Aspose::Words::IBorderAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Resets to default row formatting. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | True if the text in a table row is allowed to split across a page break. |
| [get_Borders](./get_borders/)() | Gets the collection of default cell borders for the row. |
| [get_HeadingFormat](./get_headingformat/)() | True if the row is repeated as a table heading on every page when the table spans more than one page. |
| [get_Height](./get_height/)() | Gets or sets the height of the table row in points. |
| [get_HeightRule](./get_heightrule/)() | Gets or sets the rule for determining the height of the table row. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Setter for [Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_HeadingFormat](./set_headingformat/)(bool) | Setter for [Aspose::Words::Tables::RowFormat::get_HeadingFormat](./get_headingformat/). |
| [set_Height](./set_height/)(double) | Setter for [Aspose::Words::Tables::RowFormat::get_Height](./get_height/). |
| [set_HeightRule](./set_heightrule/)(Aspose::Words::HeightRule) | Setter for [Aspose::Words::Tables::RowFormat::get_HeightRule](./get_heightrule/). |
| static [Type](./type/)() |  |

## Examples



Shows how to build a table with custom borders. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Setting table formatting options for a document builder
// will apply them to every row and cell that we add with it.
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

// Changing the formatting will apply it to the current cell,
// and any new cells that we create with the builder afterward.
// This will not affect the cells that we have added previously.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Increase row height to fit the vertical text.
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


Shows how to modify the format of rows and cells in a table. 
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

// Use the first row's "RowFormat" property to modify the formatting
// of the contents of all cells in this row.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Use the "CellFormat" property of the first cell in the last row to modify the formatting of that cell's contents.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Shows how to modify formatting of a table row. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Use the first row's "RowFormat" property to set formatting that modifies that entire row's appearance.
System::SharedPtr<Aspose::Words::Tables::Row> firstRow = table->get_FirstRow();
firstRow->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::None);
firstRow->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
firstRow->get_RowFormat()->set_AllowBreakAcrossPages(true);

doc->Save(get_ArtifactsDir() + u"Table.RowFormat.docx");
```

## See Also

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
