---
title: Aspose::Words::Tables::CellFormat class
linktitle: CellFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::CellFormat class. Represents all formatting for a table cell. To learn more, visit the  documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.tables/cellformat/
---
## CellFormat class


Represents all formatting for a table cell. To learn more, visit the [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) documentation article.

```cpp
class CellFormat : public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Resets to default cell formatting. Does not change the width of the cell. |
| [get_Borders](./get_borders/)() | Gets collection of borders of the cell. |
| [get_BottomPadding](./get_bottompadding/)() | Returns or sets the amount of space (in points) to add below the contents of cell. |
| [get_FitText](./get_fittext/)() | If **true**, fits text in the cell, compressing each paragraph to the width of the cell. |
| [get_HideMark](./get_hidemark/)() | Returns visibility of cell mark. |
| [get_HorizontalMerge](./get_horizontalmerge/)() | Specifies how the cell is merged horizontally with other cells in the row. |
| [get_LeftPadding](./get_leftpadding/)() | Returns or sets the amount of space (in points) to add to the left of the contents of cell. |
| [get_Orientation](./get_orientation/)() | Returns or sets the orientation of text in a table cell. |
| [get_PreferredWidth](./get_preferredwidth/)() | Returns or sets the preferred width of the cell. |
| [get_RightPadding](./get_rightpadding/)() | Returns or sets the amount of space (in points) to add to the right of the contents of cell. |
| [get_Shading](./get_shading/)() | Returns a [Shading](../../aspose.words/shading/) object that refers to the shading formatting for the cell. |
| [get_TopPadding](./get_toppadding/)() | Returns or sets the amount of space (in points) to add above the contents of cell. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Returns or sets the vertical alignment of text in the cell. |
| [get_VerticalMerge](./get_verticalmerge/)() | Specifies how the cell is merged with other cells vertically. |
| [get_Width](./get_width/)() | Gets the width of the cell in points. |
| [get_WrapText](./get_wraptext/)() | If **true**, wrap text for the cell. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Setter for [Aspose::Words::Tables::CellFormat::get_BottomPadding](./get_bottompadding/). |
| [set_FitText](./set_fittext/)(bool) | Setter for [Aspose::Words::Tables::CellFormat::get_FitText](./get_fittext/). |
| [set_HideMark](./set_hidemark/)(bool) | Sets visibility of cell mark. |
| [set_HorizontalMerge](./set_horizontalmerge/)(Aspose::Words::Tables::CellMerge) | Setter for [Aspose::Words::Tables::CellFormat::get_HorizontalMerge](./get_horizontalmerge/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Setter for [Aspose::Words::Tables::CellFormat::get_LeftPadding](./get_leftpadding/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::TextOrientation) | Setter for [Aspose::Words::Tables::CellFormat::get_Orientation](./get_orientation/). |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Setter for [Aspose::Words::Tables::CellFormat::get_PreferredWidth](./get_preferredwidth/). |
| [set_RightPadding](./set_rightpadding/)(double) | Setter for [Aspose::Words::Tables::CellFormat::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Setter for [Aspose::Words::Tables::CellFormat::get_TopPadding](./get_toppadding/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Setter for [Aspose::Words::Tables::CellFormat::get_VerticalAlignment](./get_verticalalignment/). |
| [set_VerticalMerge](./set_verticalmerge/)(Aspose::Words::Tables::CellMerge) | Setter for [Aspose::Words::Tables::CellFormat::get_VerticalMerge](./get_verticalmerge/). |
| [set_Width](./set_width/)(double) | Setter for [Aspose::Words::Tables::CellFormat::get_Width](./get_width/). |
| [set_WrapText](./set_wraptext/)(bool) | Setter for [Aspose::Words::Tables::CellFormat::get_WrapText](./get_wraptext/). |
| [SetPaddings](./setpaddings/)(double, double, double, double) | Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell. |
| static [Type](./type/)() |  |

## Examples



Shows how to build a table with custom borders. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->StartTable();

// Setting table formatting options for a document builder
// will apply them to every row and cell that we add with it.
builder->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(LineStyle::Engrave3D);
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
builder->get_CellFormat()->set_Orientation(TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertTable.docx");
```


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


Shows how to modify formatting of a table cell. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");
SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
SharedPtr<Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// Use a cell's "CellFormat" property to set formatting that modifies the appearance of that cell.
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(ArtifactsDir + u"Table.CellFormat.docx");
```

## See Also

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
